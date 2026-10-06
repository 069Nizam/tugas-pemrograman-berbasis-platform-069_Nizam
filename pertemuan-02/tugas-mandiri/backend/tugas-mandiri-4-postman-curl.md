# Tugas Mandiri 4 — Pengujian API dengan Postman dan curl

## Identitas

| Keterangan | Isi |
|---|---|
| Nama | Mohammad Khoirun Nizam |
| NIM | 2024520069 |
| Pertemuan | 2 |
| Tugas | Tugas Mandiri 4 |

## Tujuan

Tugas ini bertujuan untuk melakukan pengujian API menggunakan Postman dan curl serta memahami perbedaan informasi yang ditampilkan oleh masing-masing alat.

# A. Pengujian Menggunakan Postman

## 1. GET

Request:

```text
GET https://httpbin.org/get
```

Request GET digunakan untuk meminta data dari endpoint `/get`.

HTTPBin memberikan response berupa JSON yang berisi informasi request yang diterima server.

## 2. POST

Request:

```text
POST https://httpbin.org/post
```

Body menggunakan format JSON:

```json
{
  "nama": "Nizam",
  "kelas": "Informatika"
}
```

HTTPBin mengembalikan data JSON yang dikirim pada response beserta informasi request lainnya.

## Perbandingan GET dan POST

| Aspek | GET | POST |
|---|---|---|
| Method | GET | POST |
| Endpoint | `/get` | `/post` |
| Data | Tidak menggunakan request body | Menggunakan request body |
| Tujuan | Mengambil atau menguji data | Mengirim data |
| Response | Informasi request | Informasi request dan data yang dikirim |

## Screenshot Postman GET

![Postman GET](https://github.com/069Nizam/tugas-pemrograman-berbasis-platform-069_Nizam/blob/main/pertemuan-02/tugas-mandiri/screenhoots/tm4-postman-get.png)

## Screenshot Postman POST

![Postman POST](https://github.com/069Nizam/tugas-pemrograman-berbasis-platform-069_Nizam/blob/main/pertemuan-02/tugas-mandiri/screenhoots/tm4-postman-post.png)

# B. Pengujian Menggunakan curl

## 1. curl -i GET

Perintah:

```bash
curl -i https://httpbin.org/get
```

Opsi `-i` digunakan untuk menampilkan HTTP response header bersama dengan response body.

Informasi yang dapat diamati antara lain:

```text
HTTP/...
Content-Type
Content-Length
```

## 2. curl -i Status 404

Perintah:

```bash
curl -i https://httpbin.org/status/404
```

Perintah tersebut meminta HTTPBin mengembalikan status code 404. Opsi `-i` membuat response header ikut ditampilkan.

## Screenshot curl -i

![curl -i](https://github.com/069Nizam/tugas-pemrograman-berbasis-platform-069_Nizam/blob/main/pertemuan-02/tugas-mandiri/screenhoots/tm4-curl-i.png)

# C. Perbandingan curl -s dan curl -i

## curl -s

Perintah:

```bash
curl -s https://httpbin.org/get
```

Opsi `-s` atau silent digunakan untuk mengurangi output tambahan dari curl seperti progress meter. Hasil utama berupa response body lebih mudah dilihat.

## curl -i

Perintah:

```bash
curl -i https://httpbin.org/get
```

Opsi `-i` digunakan untuk menampilkan response header bersama dengan response body.

## Perbedaan

Perintah `curl -s` digunakan ketika ingin melihat response body tanpa tampilan progress meter dari curl. Sementara itu, `curl -i` digunakan ketika ingin melihat response header dan response body sekaligus. Opsi `-s` berguna untuk mendapatkan output yang lebih bersih, sedangkan `-i` berguna ketika ingin memeriksa informasi HTTP seperti status code dan Content-Type. Keduanya dapat digunakan sesuai kebutuhan pengujian API.

## Screenshot curl -s

![curl -s](https://github.com/069Nizam/tugas-pemrograman-berbasis-platform-069_Nizam/blob/main/pertemuan-02/tugas-mandiri/screenhoots/tm4-curl-s.png)

## Kesimpulan

Postman menyediakan antarmuka grafis untuk melakukan pengujian API, sedangkan curl dapat digunakan melalui terminal. Keduanya dapat digunakan untuk mengirim request dan melihat response dari server. curl juga menyediakan opsi seperti `-s` dan `-i` untuk mengatur informasi yang ditampilkan pada terminal.
