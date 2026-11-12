# Bookshelf API

RESTful API untuk mencatat buku (CRUD) yang dibangun dengan Node.js dan framework Hapi. Project ini dibuat sebagai submission kelas **Belajar Back-End Pemula dengan JavaScript** di Dicoding.

## Fitur
- Menambah buku baru dengan ID yang dibuat otomatis (nanoid)
- Melihat seluruh buku, atau satu buku berdasarkan ID
- Mengubah dan menghapus buku
- Validasi data: nama buku wajib diisi, dan `readPage` tidak boleh lebih besar dari `pageCount`
- Status `finished` dihitung otomatis dari `pageCount` dan `readPage`
- Filter daftar buku berdasarkan nama, status membaca, dan status selesai dibaca
- CORS diaktifkan untuk semua origin

## Teknologi
- Node.js
- Hapi (`@hapi/hapi`)
- nanoid
- ESLint (airbnb-base)

## Endpoint

| Method | Path | Fungsi |
|--------|------|--------|
| POST | `/books` | Menambah buku |
| GET | `/books` | Melihat semua buku (mendukung query `name`, `reading`, `finished`) |
| GET | `/books/{bookId}` | Melihat detail satu buku |
| PUT | `/books/{bookId}` | Mengubah buku |
| DELETE | `/books/{bookId}` | Menghapus buku |

Contoh filter: `GET /books?name=dicoding&reading=1&finished=0`

## Cara Menjalankan
1. Pastikan Node.js sudah terpasang.
2. Clone repository ini.
3. Pasang dependensi:
4. jalankan server:
5. Server berjalan di `http://localhost:9000`.

## Catatan
Data buku disimpan di memori (array), sehingga akan hilang saat server dihentikan.

## Pembuat
Ayub Assabiq
- GitHub: [github.com/kuyub](https://github.com/kuyub)
