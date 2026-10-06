# Tugas Mandiri 3 — Memahami Request dan Response

## Identitas

| Keterangan | Isi |
|---|---|
| Nama | Mohammad Khoirun Nizam |
| NIM | 2024520069 |
| Pertemuan | 2 |
| Tugas | Tugas Mandiri 3 |

## Tujuan

Tugas ini bertujuan untuk memahami request dan response serta melihat data yang dikirim client dan diterima server.

## Pengujian GET

Endpoint yang digunakan:

```text
https://httpbin.org/get?nama=Nizam&kelas=Informatika
```

Query parameter yang digunakan:

```text
nama=Nizam
kelas=Informatika
```

HTTPBin akan mengembalikan informasi request yang diterima server. Query parameter dapat dilihat pada bagian `args` pada response JSON.

Contoh struktur response:

```json
{
  "args": {
    "nama": "Nizam",
    "kelas": "Informatika"
  },
  "headers": {},
  "origin": "...",
  "url": "https://httpbin.org/get?nama=Nizam&kelas=Informatika"
}
```

## Pengujian Headers

Endpoint yang digunakan:

```text
https://httpbin.org/headers
```

Endpoint tersebut digunakan untuk melihat HTTP header yang diterima oleh server.

Response akan menampilkan informasi header yang dikirim oleh client kepada HTTPBin.

## Request dan Response

Alur komunikasi dapat digambarkan sebagai berikut:

```text
Client
   |
   | Request
   | Method + URL + Header + Body
   v
Server
   |
   | Response
   | Status Code + Header + Body
   v
Client
```

## Jawaban Pertanyaan

### 1. Apa yang dimaksud request?

Request adalah permintaan yang dikirim oleh client kepada server untuk melakukan suatu operasi. Request dapat berisi HTTP method, URL, header, query parameter, dan request body.

### 2. Apa yang dimaksud response?

Response adalah hasil yang diberikan server setelah menerima dan memproses request dari client. Response dapat berisi status code, header, dan response body.

### 3. Apa fungsi query parameter?

Query parameter digunakan untuk mengirimkan informasi tambahan melalui URL. Query parameter biasanya digunakan untuk memberikan nilai yang dibutuhkan server untuk melakukan pencarian, penyaringan, atau pemrosesan data.

### 4. Apa fungsi HTTP header?

HTTP header digunakan untuk membawa informasi tambahan dalam komunikasi antara client dan server. Header dapat berisi informasi seperti jenis data, autentikasi, user agent, dan informasi lainnya.

### 5. Apa perbedaan data pada URL dengan data pada request body?

Data pada URL dapat terlihat langsung pada alamat request, misalnya query parameter setelah tanda `?`. Data pada request body dikirim sebagai bagian dari isi request dan biasanya digunakan untuk mengirim data yang lebih terstruktur seperti JSON.

## Screenshot

### Response /get

![Response GET](https://github.com/069Nizam/tugas-pemrograman-berbasis-platform-069_Nizam/blob/main/pertemuan-02/tugas-mandiri/screenhoots/tm3-get.png)

### Response /headers

![Response Headers](https://github.com/069Nizam/tugas-pemrograman-berbasis-platform-069_Nizam/blob/main/pertemuan-02/tugas-mandiri/screenhoots/tm3-headers.png)

## Kesimpulan

Request merupakan data yang dikirim client kepada server, sedangkan response merupakan hasil yang diberikan server kepada client. Query parameter digunakan untuk mengirim data melalui URL, sedangkan HTTP header digunakan untuk membawa informasi tambahan dalam komunikasi HTTP.
