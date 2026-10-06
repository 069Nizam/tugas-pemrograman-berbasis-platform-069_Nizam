# Tugas Mandiri 1 — Mengenal HTTP Method dan Endpoint

## Identitas

| Keterangan | Isi |
|---|---|
| Nama | Mohammad Khoirun Nizam |
| NIM | 2024520069 |
| Pertemuan | 2 |
| Tugas | Tugas Mandiri 1 |

## Tujuan

Tugas ini bertujuan untuk memahami hubungan antara HTTP method, endpoint, parameter, request, dan response menggunakan layanan HTTPBin.

## Pengujian Endpoint

### 1. GET /get

**HTTP Method:** GET

**URL:**

```text
https://httpbin.org/get?nama=Nizam&kelas=Informatika
```

**Tujuan:** Menguji request GET dan mengirimkan data melalui query parameter.

**Data yang dikirim:**

```text
nama=Nizam
kelas=Informatika
```

**Status Code:** 200 OK

**Response Body:** HTTPBin mengembalikan informasi request dalam format JSON, termasuk query parameter yang dikirim.

**Informasi yang dikembalikan server:** URL, args atau query parameter, headers, origin, dan informasi request lainnya.

---

### 2. POST /post

**HTTP Method:** POST

**URL:**

```text
https://httpbin.org/post
```

**Tujuan:** Menguji pengiriman data melalui request body.

**Data yang dikirim:**

```json
{
  "nama": "Nizam",
  "kelas": "Informatika"
}
```

**Status Code:** 200 OK

**Response Body:** HTTPBin mengembalikan informasi request dan data JSON yang dikirim.

**Informasi yang dikembalikan server:** Data JSON pada bagian JSON, headers, URL, origin, dan informasi request lainnya.

---

### 3. PUT /put

**HTTP Method:** PUT

**URL:**

```text
https://httpbin.org/put
```

**Tujuan:** Menguji request PUT untuk mengirim data yang biasanya digunakan untuk memperbarui data.

**Data yang dikirim:**

```json
{
  "nama": "Nizam",
  "kelas": "Informatika"
}
```

**Status Code:** 200 OK

**Response Body:** HTTPBin mengembalikan informasi request dan data yang dikirim.

**Informasi yang dikembalikan server:** Data JSON, headers, URL, origin, dan informasi request lainnya.

---

### 4. PATCH /patch

**HTTP Method:** PATCH

**URL:**

```text
https://httpbin.org/patch
```

**Tujuan:** Menguji request PATCH untuk mengirim data yang biasanya digunakan untuk memperbarui sebagian data.

**Data yang dikirim:**

```json
{
  "kelas": "Informatika"
}
```

**Status Code:** 200 OK

**Response Body:** HTTPBin mengembalikan informasi request dan data yang dikirim.

**Informasi yang dikembalikan server:** Data JSON, headers, URL, origin, dan informasi request lainnya.

---

### 5. DELETE /delete

**HTTP Method:** DELETE

**URL:**

```text
https://httpbin.org/delete
```

**Tujuan:** Menguji request DELETE.

**Data yang dikirim:** Tidak ada.

**Status Code:** 200 OK

**Response Body:** HTTPBin mengembalikan informasi request yang diterima server.

**Informasi yang dikembalikan server:** Headers, URL, origin, dan informasi request lainnya.

## Tabel Hasil Pengujian

| No | Method | Endpoint | Data yang dikirim | Status | Hasil |
|---:|---|---|---|---:|---|
| 1 | GET | `/get` | Query parameter `nama` dan `kelas` | 200 | Server mengembalikan query parameter dan informasi request dalam JSON. |
| 2 | POST | `/post` | JSON/body | 200 | Server mengembalikan data JSON yang dikirim dan informasi request. |
| 3 | PUT | `/put` | JSON/body | 200 | Server mengembalikan data JSON yang dikirim dan informasi request. |
| 4 | PATCH | `/patch` | JSON/body | 200 | Server mengembalikan data JSON yang dikirim dan informasi request. |
| 5 | DELETE | `/delete` | Tidak ada | 200 | Server mengembalikan informasi request DELETE. |

## Screenshot Pengujian

### GET

![Hasil pengujian GET](../../kegiatan-praktikum/screenshots/tm1-postman-get.png)

### POST

![Hasil pengujian POST](../../kegiatan-praktikum/screenshots/tm1-postman-post.png)

## Kesimpulan

HTTP method menentukan jenis operasi yang dilakukan client terhadap endpoint. GET digunakan untuk mengambil data, POST digunakan untuk mengirim data baru, PUT dan PATCH digunakan untuk memperbarui data, sedangkan DELETE digunakan untuk menghapus data. HTTPBin membantu melihat kembali informasi request yang diterima server sehingga hubungan antara method, endpoint, data, dan response dapat dipahami dengan lebih jelas.
