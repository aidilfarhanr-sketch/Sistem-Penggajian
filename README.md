# Sistem Penggajian — Rarestore

Sistem Penggajian Rarestore adalah aplikasi web sederhana berbasis HTML, CSS, dan JavaScript untuk membantu pengelolaan data karyawan, absensi harian, proses penggajian, riwayat gaji, slip gaji, serta laporan grafik.

Proyek ini dibuat sebagai sistem manajemen penggajian yang dapat dijalankan langsung melalui browser tanpa instalasi backend tambahan. Data demo disimpan menggunakan `localStorage` browser, sehingga cocok untuk kebutuhan presentasi, demo, dan pengembangan awal.

---

## Link Akses Website

Jika GitHub Pages sudah diaktifkan, website dapat diakses melalui link berikut:

https://aidilfarhanr-sketch.github.io/Sistem-Penggajian/

Jika link belum bisa dibuka, aktifkan dulu GitHub Pages melalui:

`Settings` → `Pages` → `Build and deployment` → `Deploy from a branch` → pilih branch `main` dan folder `/root` → `Save`.

---

## Login Demo

Gunakan akun berikut untuk masuk ke sistem:

| Keterangan | Data |
|---|---|
| ID Pengguna | `aidilfarhan` |
| Password | `22122001` |
| Role | Administrator |

Catatan: akun ini digunakan untuk demo. Untuk penggunaan production, password sebaiknya tidak ditulis langsung di file frontend dan perlu dipindahkan ke sistem autentikasi backend/database.

---

## Fitur Utama

### 1. Login Administrator
Sistem memiliki halaman login dengan tampilan modern. Pengguna harus memasukkan ID dan password sebelum masuk ke dashboard.

### 2. Dashboard Ringkasan
Dashboard menampilkan ringkasan data penggajian, estimasi total gaji bersih, status karyawan hari ini, rekap absensi, dan grafik gaji.

### 3. Manajemen Karyawan
Admin dapat melihat daftar karyawan, menambah karyawan baru, mengedit nama, jabatan, gaji pokok, warna avatar, dan menghapus data karyawan.

### 4. Absensi Harian
Admin dapat mencatat status kehadiran karyawan setiap hari dengan pilihan:

- Hadir
- Sakit
- Alpa

Data absensi digunakan untuk menghitung potongan gaji otomatis.

### 5. Riwayat Absensi
Sistem menyediakan halaman riwayat absensi per bulan dan per karyawan, sehingga admin bisa melihat rekapan kehadiran secara lebih rapi.

### 6. Proses Penggajian
Sistem menghitung gaji bersih berdasarkan gaji pokok dan potongan absensi:

- Hadir: tidak ada potongan
- Sakit: potongan 1% per hari
- Alpa: potongan 3% per hari

Setelah diproses, data penggajian akan masuk ke riwayat gaji.

### 7. Riwayat Gaji dan Slip Gaji
Admin dapat melihat riwayat penggajian, membuka slip gaji karyawan, mencetak slip, dan menyimpan slip sebagai PDF melalui fitur print browser.

### 8. Laporan dan Grafik
Sistem menyediakan grafik untuk membantu membaca kondisi penggajian dan absensi, seperti:

- Gaji pokok vs gaji bersih
- Distribusi gaji bersih
- Rekap absensi
- Tren penggajian bulanan
- Potongan per karyawan

### 9. Export Data
Sistem mendukung export data ke CSV untuk:

- Data karyawan
- Data absensi
- Data penggajian

---

## Struktur File

```text
Sistem-Penggajian/
├── index.html
└── README.md
```

Keterangan:

- `index.html` adalah file utama aplikasi.
- `README.md` adalah dokumentasi proyek untuk GitHub.

---

## Cara Menjalankan di Laptop

1. Download atau clone repository ini.
2. Buka folder proyek.
3. Klik dua kali file `index.html`.
4. Login menggunakan akun demo yang tersedia di atas.
5. Sistem siap digunakan untuk demo.

---

## Cara Upload ke GitHub

### Opsi 1 — Upload Manual dari Website GitHub

1. Buka repository:

   https://github.com/aidilfarhanr-sketch/Sistem-Penggajian

2. Klik tombol `Add file`.
3. Pilih `Upload files`.
4. Upload file berikut:

   - `index.html`
   - `README.md`

5. Scroll ke bawah.
6. Isi pesan commit, misalnya:

   `Upload Sistem Penggajian`

7. Klik `Commit changes`.

### Opsi 2 — Upload Menggunakan Git CMD

Jalankan perintah berikut di folder proyek:

```bash
git init
git add .
git commit -m "Upload Sistem Penggajian"
git branch -M main
git remote add origin https://github.com/aidilfarhanr-sketch/Sistem-Penggajian.git
git push -u origin main
```

Jika remote sudah pernah ditambahkan, gunakan:

```bash
git remote set-url origin https://github.com/aidilfarhanr-sketch/Sistem-Penggajian.git
git push -u origin main
```

---

## Cara Mengaktifkan GitHub Pages

1. Buka repository di GitHub.
2. Masuk ke menu `Settings`.
3. Pilih menu `Pages`.
4. Pada bagian `Build and deployment`, pilih `Deploy from a branch`.
5. Pada bagian branch, pilih:

   - Branch: `main`
   - Folder: `/root`

6. Klik `Save`.
7. Setelah aktif, buka link:

   https://aidilfarhanr-sketch.github.io/Sistem-Penggajian/

---

## Teknologi yang Digunakan

- HTML5
- CSS3
- JavaScript
- Chart.js
- LocalStorage
- Google Fonts

---

## Catatan Penting

Sistem ini masih berbasis frontend/static demo. Artinya data tersimpan di browser masing-masing pengguna melalui `localStorage`. Jika browser dibersihkan atau data situs dihapus, maka data absensi, karyawan tambahan, dan riwayat gaji bisa hilang.

Untuk versi production, sistem sebaiknya dikembangkan menggunakan backend dan database seperti PHP/MySQL, Laravel, Node.js, atau teknologi lain agar data tersimpan lebih aman dan terpusat.

---

## Author

Dibuat oleh **Aidil Farhan Rares**.
