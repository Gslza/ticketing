# 📌 Aplikasi Ticketing Wisata (Java Desktop)

## 1. Deskripsi Aplikasi
Aplikasi Ticketing Wisata merupakan aplikasi berbasis **Java Desktop (NetBeans)** yang digunakan untuk mengelola data tempat wisata, data pengunjung, serta transaksi pemesanan tiket wisata.  
Aplikasi ini terhubung dengan database **MySQL** bernama `db_ticket`.

---

## 2. Tujuan Aplikasi
- Mempermudah pengelolaan data wisata
- Mempermudah pendataan pengunjung
- Mengotomatisasi proses pemesanan tiket
- Mengurangi kesalahan perhitungan harga tiket

---

## 3. Teknologi yang Digunakan
- Bahasa Pemrograman : Java (Swing)
- IDE : NetBeans
- Database : MySQL
- Library Database : MySQL Connector/J

---

## 4. Struktur Database

### Database

db_ticket


### Tabel `wisata`
| Field | Tipe |
|------|------|
| id_wisata | INT (PK, AI) |
| nama_wisata | VARCHAR |
| lokasi | VARCHAR |
| harga_tiket | INT |

### Tabel `pengunjung`
| Field | Tipe |
|------|------|
| id_pengunjung | INT (PK, AI) |
| nama_pengunjung | VARCHAR |
| no_hp | VARCHAR |

### Tabel `tiket`
| Field | Tipe |
|------|------|
| id_tiket | INT (PK, AI) |
| id_wisata | INT (FK) |
| id_pengunjung | INT (FK) |
| jumlah_tiket | INT |
| total_harga | INT |
| tanggal | DATE |

---

## 5. Struktur Form Aplikasi

### 5.1 Menu Utama
Menu utama berfungsi sebagai navigasi utama aplikasi.

Menu:
- Master Data
  - Data Wisata
  - Data Pengunjung
- Transaksi
  - Pemesanan Tiket
- Keluar

---

### 5.2 Form Data Wisata
Digunakan untuk mengelola data tempat wisata.

Fungsi:
- Menambah data wisata
- Mengubah data wisata
- Menghapus data wisata
- Menampilkan data wisata dalam tabel

Data disimpan pada tabel `wisata`.

---

### 5.3 Form Data Pengunjung
Digunakan untuk mengelola data pengunjung.

Fungsi:
- Menambah data pengunjung
- Mengubah data pengunjung
- Menghapus data pengunjung
- Menampilkan data pengunjung dalam tabel

Data disimpan pada tabel `pengunjung`.

---

### 5.4 Form Pemesanan Tiket
Digunakan untuk melakukan transaksi pemesanan tiket wisata.

Fungsi:
- Memilih data wisata
- Memilih data pengunjung
- Menginput jumlah tiket
- Menghitung total harga otomatis
- Menyimpan transaksi pemesanan

Data disimpan pada tabel `tiket`.

---

## 6. Alur Cara Kerja Sistem

1. Pengguna menjalankan aplikasi
2. Sistem menampilkan Menu Utama
3. Pengguna menginput data wisata
4. Pengguna menginput data pengunjung
5. Pengguna melakukan pemesanan tiket
6. Sistem menghitung total harga secara otomatis
7. Data transaksi disimpan ke database
8. Pengguna dapat keluar dari aplikasi

---

## 7. Alur Perhitungan Harga
Total Harga = Harga Tiket × Jumlah Tike

Perhitungan dilakukan secara otomatis menggunakan event `KeyReleased` pada field jumlah tiket.

---

## 8. Kelebihan Aplikasi
- Menggunakan database terpusat
- Data saling terhubung (relasional)
- Perhitungan otomatis
- Antarmuka sederhana dan mudah digunakan
- Mudah dikembangkan lebih lanjut

---

## 9. Kesimpulan
Aplikasi Ticketing Wisata ini mampu membantu proses pengelolaan data wisata dan pemesanan tiket secara efektif dan efisien. Dengan menggunakan Java Desktop dan MySQL, aplikasi ini memenuhi kebutuhan dasar sistem informasi ticketing wisata.

---
