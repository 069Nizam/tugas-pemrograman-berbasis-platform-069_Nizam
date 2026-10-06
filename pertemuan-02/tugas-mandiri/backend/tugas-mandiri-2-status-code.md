# Tugas Mandiri 2 — Memahami HTTP Status Code

## Identitas

| Keterangan | Isi |
|---|---|
| Nama | Mohammad Khoirun Nizam |
| NIM | 2024520069 |
| Pertemuan | 2 |
| Tugas | Tugas Mandiri 2 |

## Tujuan

Tugas ini bertujuan untuk memahami arti HTTP status code dan mengetahui kondisi yang ditunjukkan oleh server melalui status code.

## Endpoint Pengujian

Pengujian dilakukan menggunakan endpoint HTTPBin:

```text
https://httpbin.org/status/:code
```

Contoh:

```text
https://httpbin.org/status/200
```

## Hasil Pengujian

| Status Code | Arti | Hasil Pengujian | Kapan Digunakan |
|---:|---|---|---|
| 200 | OK | Server berhasil memproses request. | Ketika request berhasil diproses. |
| 201 | Created | Server berhasil membuat resource baru. | Ketika data atau resource baru berhasil dibuat. |
| 400 | Bad Request | Request tidak dapat diproses karena terdapat kesalahan pada request. | Ketika client mengirim request yang tidak valid. |
| 401 | Unauthorized | Request membutuhkan autentikasi yang valid. | Ketika client belum memberikan autentikasi atau autentikasinya tidak valid. |
| 403 | Forbidden | Server memahami request tetapi menolak memberikan akses. | Ketika client tidak memiliki izin untuk mengakses resource. |
| 404 | Not Found | Resource atau endpoint yang diminta tidak ditemukan. | Ketika resource yang diminta tidak tersedia. |
| 500 | Internal Server Error | Terjadi kesalahan pada sisi server. | Ketika server mengalami masalah saat memproses request. |

## Pertanyaan

### 1. Apa perbedaan 400 dan 404?

Status code 400 menunjukkan bahwa request yang dikirim client tidak valid sehingga server tidak dapat memprosesnya. Status code 404 menunjukkan bahwa request dapat diterima tetapi resource atau endpoint yang diminta tidak ditemukan.

### 2. Apa perbedaan 401 dan 403?

Status code 401 menunjukkan bahwa client membutuhkan autentikasi atau autentikasi yang diberikan tidak valid. Status code 403 menunjukkan bahwa client sudah dikenali atau request dipahami tetapi client tidak memiliki izin untuk mengakses resource tersebut.

### 3. Mengapa 500 menunjukkan masalah pada sisi server?

Status code 500 termasuk kategori server error. Status ini menunjukkan bahwa server mengalami masalah ketika memproses request sehingga request tidak dapat diselesaikan dengan normal.

### 4. Apakah semua error HTTP berarti server mengalami kerusakan?

Tidak. Tidak semua error HTTP berarti server mengalami kerusakan. Beberapa error terjadi karena request atau kondisi dari sisi client, seperti 400, 401, 403, dan 404. Status 500 menunjukkan masalah yang terjadi pada sisi server.

## Screenshot Pengujian

### Status 200

![Status 200](https://github.com/069Nizam/tugas-pemrograman-berbasis-platform-069_Nizam/blob/main/pertemuan-02/tugas-mandiri/screenhoots/tm2-status-200.png)

### Status 404

![Status 404](https://github.com/069Nizam/tugas-pemrograman-berbasis-platform-069_Nizam/blob/main/pertemuan-02/tugas-mandiri/screenhoots/tm2-status-404.png)

### Status 500

![Status 500](https://github.com/069Nizam/tugas-pemrograman-berbasis-platform-069_Nizam/blob/main/pertemuan-02/tugas-mandiri/screenhoots/tm2-status-500.png)

## Kesimpulan

HTTP status code memberikan informasi mengenai hasil pemrosesan request. Status 200 dan 201 menunjukkan keberhasilan, status 400 sampai 404 pada pengujian menunjukkan berbagai kondisi kesalahan dari request atau akses, sedangkan status 500 menunjukkan kesalahan pada sisi server.
