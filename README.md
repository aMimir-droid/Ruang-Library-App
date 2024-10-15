# Library App

## Assignment Library App

### NOTES

- Pada skeleton kode yang terdapat file `main.test.js` tidak boleh diubah sama sekali.
- Dilarang mengganti nama function yang diberikan.
- Dilarang mengganti struktur dari skeleton kode yang diberikan.
- Dilarang untuk mengedit file `initial.json` yang terdapat pada folder `server`.
- Wajib menjalankan `npm install` atau `pnpm install` sebelum mengerjakan.

### Objectives

- Dapat menggunakan DOM untuk membuat _website_.
- Dapat melakukan call API.

### Description

Pada Assignment kali ini kalian akan diminta untuk membuat sebuah _website_ yang dapat melakukan operasi CRUD (Create, Read, Update, Delete) data buku untuk sebuah perpustakaan.

Komunikasi data antara _website_ dengan _server_ menggunakan _API_.

Beberapa hal yang sudah disediakan untuk membantu kalian dalam menyelesaikan _website_ ini:

- API Server sudah disediakan pada folder `server` dengan nama file `library-db.json`. API Server ini menggunakan [json-server](https://www.npmjs.com/package/json-server) yang dapat kalian jalankan
  dengan menggunakan command `pnpm start:server`.

  > server akan berjalan pada `http://localhost:3333`

  API Server ini memiliki beberapa _endpoint_, antara lain:

  - **GET /books (untuk mendapatkan seluruh data buku)**

    Example Result:

    ```JSON
    [
        {
            "id": 1,
            "title": "Buku A",
            "author": "Author A",
            "year": 2020,
            "quantity": 10
        },
        {
            "id": 2,
            "title": "Buku B",
            "author": "Author B",
            "year": 2020,
            "quantity": 10
        }
    ]
    ```

  - **POST /books (untuk menambahkan data buku)**

    Payload yang dikirimkan harus memiliki format sebagai berikut:

    ```json
    {
      "title": "string",
      "author": "string",
      "year": "number",
      "quantity": "number"
    }
    ```

  - **PUT /books/id (untuk mengubah data buku)**

    Payload yang dikirimkan harus memiliki format sebagai berikut:

    ```json
    {
      "title": "string",
      "author": "string",
      "year": "number",
      "quantity": "number"
    }
    ```

  - **DELETE /books/id (untuk menghapus data buku berdasarkan id)**

    Jika id ditemukan maka akan menghapus data buku dan mengembalikan response status code 200.

- Skeleton code client sudah disediakan pada folder `client` dengan nama file `main.js`. Kalian hanya perlu mengimplementasikan kode yang dibutuhkan untuk menyelesaikan _website_ ini. Beberapa
  function sudah disediakan comment yang menjelaskan apa yang harus dilakukan oleh function tersebut. Untuk menjalankan client bisa menggunakan command `pnpm start:client`.

  > client akan berjalan pada `http://localhost:3000`

---

Web Application ini akan berjalan dengan general requirements sebagai berikut:

1. Ketika halaman web di render pertama kali, data buku pada _database_ secara otomatis di tampilkan kedalam _table_.
2. Ketika tombol "Add Book" di klik maka tampilan akan berubah menjadi _form_ untuk menambahkan data buku. Ketika _form_ di submit maka data buku akan di tambahkan kedalam _database_ dan data terbaru
   akan langsung di tampilkan secara _realtime_ tanpa perlu melakukan _refresh_ halaman.
3. Ketika tombol "Edit" di klik maka tampilan akan berubah menjadi _form_ untuk mengubah data buku. Semua informasi mengenai buku yang akan di edit sudah berada di dalam _form input_. Ketika _form_ di
   submit maka data buku akan di ubah kedalam _database_ dan data terbaru akan langsung di tampilkan secara _realtime_ tanpa perlu melakukan _refresh_ halaman.
4. Ketika tombol "Hapus" di klik maka akan menghapus data buku dalam _database_ dan data buku yang di _delete_ secara otomatis di hilangkan tanpa perlu melakukan _refresh_ halaman.
5. Aplikasi harus di deploy ke netlify, kemudian link deploy nya harus di jadikan variable `NetlifyDeployUrl` pada file `deployData.js`, jangan lupa sertakan nama dan CAMPID kalian pada file tersebut
   (contoh bisa dilihat didalam file tersebut)

Untuk penjelasan lebih lanjut, silahkan lihat di comment yang sudah disediakan pada skeleton code.

Video demo Applikasi:

![preview](https://youtu.be/76wCavJdTRs)
