# Pentunjuk Menjalankan Aplikasi

1. Jalankan perintah melalui terminal di folder ini

   ```
   json-server --watch db.json
   ```

2. Buka folder client. Jalan perintah melalui terminal

   ```
   npm install
   ```

   untuk menginstal dependensi aplikasi

3. Jalan perintah

   ```
   npm run start
   ```

   untuk menjalankan aplikasi dalam mode pengembangan

Catatan:

Apabila dijalan secara _default_, json server akan berjalan pada port 3000 dan aplikasi berjalan pada port yang lain. Jika terdapat permasalahan saat menjalankan aplikasi, dapat dilakukan pada pengecekan pada kode di bagian

```
client/src/hooks/useFetch.js

baris 10:		const rawData = await fetch('http://localhost:3000/items');
```

dan juga

```
client/src/components/modalAdd.js

baris 16: 	  await axios.post(`http://localhost:3000/items`, {
                  name: name,
                  cost: +cost,
                  created_at: trimmedDate,
                });
                addItem();
                setRefetch(true);
              };
```

Sesuaikan kedua alamat di kedua baris dengan alamat dan port json server yang dijalankan.
