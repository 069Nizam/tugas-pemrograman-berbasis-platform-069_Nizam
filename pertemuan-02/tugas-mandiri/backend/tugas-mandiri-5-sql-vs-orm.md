# Tugas Mandiri 5 — Membandingkan SQL Mentah dan ORM

## Identitas

| Keterangan | Isi |
|---|---|
| Nama | Mohammad Khoirun Nizam |
| NIM | 2024520069 |
| Pertemuan | 2 |
| Tugas | Tugas Mandiri 5 |

## Tujuan

Tugas ini bertujuan untuk memahami perbedaan penggunaan SQL mentah dan ORM dalam mengakses database.

## Operasi yang Dipilih

Operasi database yang digunakan adalah mengambil satu data berdasarkan ID.

Contoh tabel:

```text
jadwal
```

Contoh struktur data:

| id | mata_kuliah | hari | jam |
|---:|---|---|---|
| 1 | Pemrograman Berbasis Platform | Senin | 08:00 |
| 2 | Basis Data | Selasa | 10:00 |
| 3 | Internet of Things | Rabu | 13:00 |

# A. SQL Mentah

SQL yang digunakan:

```sql
SELECT *
FROM jadwal
WHERE id = ?;
```

Nilai parameter:

```text
1
```

Contoh penggunaan menggunakan Node.js dan mysql2:

```javascript
const [rows] = await connection.execute(
  'SELECT * FROM jadwal WHERE id = ?',
  [1]
);
```

SQL digunakan secara langsung untuk menentukan query yang dikirim ke database.

# B. ORM

Contoh menggunakan Prisma:

```javascript
const jadwal = await prisma.jadwal.findUnique({
  where: {
    id: 1
  }
});
```

Pada pendekatan ORM, programmer menggunakan method dan struktur yang disediakan ORM untuk berinteraksi dengan database.

# Perbandingan

| Aspek | SQL Mentah | ORM |
|---|---|---|
| Cara akses | Menulis query SQL secara langsung | Menggunakan method ORM |
| Kontrol query | Lebih langsung dan fleksibel | Mengikuti fitur ORM |
| Kemudahan | Membutuhkan pemahaman SQL | Lebih sederhana untuk operasi umum |
| Struktur kode | Query SQL berada di dalam kode | Menggunakan object dan method |
| Database | Sangat bergantung pada SQL database | ORM membantu mengabstraksi database |
| Pengembangan | Cocok untuk query yang membutuhkan kontrol langsung | Cocok untuk pengembangan aplikasi yang banyak menggunakan operasi CRUD |

# Jawaban Pertanyaan

## 1. Apa perbedaan SQL mentah dan ORM?

SQL mentah merupakan pendekatan ketika programmer menulis dan menjalankan query SQL secara langsung ke database. ORM merupakan pendekatan yang menggunakan library untuk mengakses database melalui object, method, dan model yang disediakan oleh ORM.

## 2. Apa kelebihan SQL mentah?

SQL mentah memberikan kontrol yang lebih langsung terhadap query database. Programmer dapat menulis query sesuai kebutuhan dan lebih mudah melakukan optimasi pada query tertentu.

## 3. Apa kelebihan ORM?

ORM membuat proses akses database lebih terstruktur dan dapat mengurangi kebutuhan menulis query SQL secara langsung untuk operasi umum. ORM juga menyediakan model dan method yang dapat membantu programmer dalam melakukan operasi CRUD.

## 4. Apa risiko SQL injection?

SQL injection adalah serangan yang terjadi ketika input dari pengguna dimasukkan ke dalam query SQL tanpa pengamanan yang tepat. Penyerang dapat memanfaatkan input tersebut untuk mengubah query dan mengakses atau memanipulasi data yang tidak seharusnya dapat diakses.

## 5. Mengapa penggunaan parameter query dapat mengurangi risiko SQL injection?

Parameter query memisahkan nilai input dari struktur perintah SQL. Dengan demikian, input pengguna diperlakukan sebagai nilai data dan bukan sebagai bagian dari perintah SQL.

Contoh:

```sql
SELECT *
FROM jadwal
WHERE id = ?;
```

Nilai `1` diberikan sebagai parameter secara terpisah sehingga tidak digabungkan langsung ke string query.

## 6. Bagaimana ORM membantu programmer dalam mengakses database?

ORM menyediakan model dan method yang dapat digunakan untuk melakukan operasi database tanpa harus menulis seluruh query SQL secara manual. ORM dapat membantu programmer dalam operasi seperti mengambil, menambahkan, mengubah, dan menghapus data.

# Kesimpulan

SQL mentah dan ORM sama-sama dapat digunakan untuk mengakses database tetapi memiliki pendekatan yang berbeda. SQL mentah memberikan kontrol yang lebih langsung terhadap query, sedangkan ORM menyediakan abstraksi sehingga operasi database dapat dilakukan melalui model dan method. Penggunaan parameter query dan fitur keamanan ORM dapat membantu mengurangi risiko SQL injection.
