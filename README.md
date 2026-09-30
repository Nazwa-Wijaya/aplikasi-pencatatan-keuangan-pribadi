# PRD Personal Finance

Sep 30, 2026 · @Nazwa wijaya

## 1. Ringkasan Produk

**Personal Finance** adalah aplikasi web yang membantu siapa pun mencatat, mengelola, dan memantau keuangan pribadi dalam satu tempat: dari uang saku sampai gaji bulanan.

> *Catat sekali, saldo terhitung otomatis, kondisi keuangan langsung terlihat.*

| Aspek | Keterangan |
| --- | --- |
| Nama produk | Personal Finance |
| Judul proyek | Rancang Bangun Aplikasi Pencatatan Keuangan Pribadi Berbasis Web |
| Platform | Aplikasi web (responsive: desktop, laptop, tablet, smartphone) |
| Target pengguna | Individu, mahasiswa, pelajar, karyawan, dan masyarakat umum |
| Nilai utama | Pencatatan terstruktur, saldo otomatis, dashboard dan laporan visual |

Dengan Personal Finance, pengguna dapat:

- Mencatat pemasukan dan pengeluaran dengan cepat.
- Mengelompokkan transaksi berdasarkan kategori.
- Melihat saldo yang dihitung otomatis.
- Memantau kondisi keuangan lewat dashboard, grafik, dan laporan periodik.

## 2. Masalah yang Diselesaikan

Banyak orang mencatat keuangan secara manual lewat catatan atau spreadsheet, atau tidak mencatat sama sekali. Akibatnya, uang terasa "habis begitu saja".

| Masalah hari ini | Dampak bagi pengguna |
| --- | --- |
| Pemasukan dan pengeluaran tidak tercatat rapi | Sulit tahu total uang yang masuk dan keluar |
| Tidak ada pengelompokan | Sulit tahu ke mana uang digunakan |
| Riwayat transaksi tersebar | Data tidak terorganisir dan sulit dicari |
| Tidak ada tampilan per periode | Sulit memantau kondisi keuangan mingguan, bulanan, atau tahunan |
| Saldo dihitung manual | Rawan salah hitung dan memakan waktu |

**Solusi:** sistem pencatatan keuangan yang terstruktur, mudah digunakan, dan menghitung semuanya secara otomatis.

## 3. Tujuan dan Batasan

### Tujuan produk

1. Memudahkan pengguna mencatat pemasukan.
2. Memudahkan pengguna mencatat pengeluaran.
3. Mengelompokkan transaksi berdasarkan kategori.
4. Menghitung saldo secara otomatis.
5. Menampilkan riwayat transaksi.
6. Menampilkan ringkasan keuangan melalui dashboard.
7. Menyediakan laporan keuangan per periode.
8. Menyediakan antarmuka yang mudah digunakan dan responsive.

### Di luar cakupan versi awal (MVP)

Fitur berikut sengaja tidak dikerjakan dulu agar MVP tetap fokus, dan dapat dikembangkan di versi berikutnya:

- Integrasi rekening bank dan e-wallet.
- Sistem investasi.
- Pembayaran tagihan langsung.
- Sistem akuntansi perusahaan.
- Prediksi keuangan berbasis AI.

## 4. Persona Pengguna

| Persona | Kebutuhan utama |
| --- | --- |
| **Mahasiswa** | Mencatat uang saku, makanan, transportasi, kebutuhan kuliah, dan hiburan |
| **Karyawan** | Mencatat gaji dan pengeluaran bulanan, memantau pengeluaran per kategori, mengetahui saldo yang tersedia |
| **Pengguna umum** | Sistem sederhana untuk mengelola keuangan sehari-hari |

## 5. Fitur Utama

### 5.1 Autentikasi

Pengguna dapat register, login, logout, dan mengubah password. Sistem memvalidasi data login sebelum memberi akses ke dashboard.

| Form | Field |
| --- | --- |
| Register | Nama, email, password, konfirmasi password |
| Login | Email, password |

*User story: sebagai pengguna baru, saya ingin membuat akun agar data keuangan saya tersimpan aman dan hanya bisa saya akses.*

### 5.2 Dashboard

Dashboard adalah halaman pertama setelah login dan menampilkan ringkasan keuangan sekilas:

- Total saldo, total pemasukan, dan total pengeluaran.
- Jumlah transaksi.
- Grafik pemasukan dan pengeluaran.
- Transaksi terbaru.

```latex
Saldo = Total\ Pemasukan - Total\ Pengeluaran
```

*User story: sebagai pengguna, saya ingin melihat kondisi keuangan saya begitu login tanpa menghitung manual.*

### 5.3 Manajemen Transaksi (CRUD)

Pengguna dapat menambah, melihat, mengubah, dan menghapus transaksi miliknya.

| Field | Wajib | Keterangan |
| --- | --- | --- |
| Jenis transaksi | Ya | `income` (pemasukan) atau `expense` (pengeluaran) |
| Nominal | Ya | Jumlah uang |
| Kategori | Ya | Sesuai jenis transaksi |
| Tanggal | Ya | Tanggal transaksi terjadi |
| Deskripsi | Tidak | Catatan tambahan |

*User story: sebagai pengguna, saya ingin mencatat transaksi dalam hitungan detik agar tidak malas mencatat.*

### 5.4 Laporan Keuangan

Pengguna dapat melihat laporan berdasarkan periode: hari ini, minggu ini, bulan ini, tahun ini, atau rentang tanggal kustom. Laporan menampilkan total pemasukan, total pengeluaran, saldo, pengeluaran per kategori, dan grafik keuangan.

### 5.5 Profil Pengguna

Pengguna dapat melihat dan mengubah nama, email, dan password.

## 6. Kategori dan Riwayat Transaksi

### Kategori bawaan

| Pemasukan (income) | Pengeluaran (expense) |
| --- | --- |
| Gaji | Makanan |
| Uang Saku | Transportasi |
| Bonus | Belanja |
| Freelance | Pendidikan |
| Penjualan | Hiburan |
| Lainnya | Kesehatan |
|  | Tagihan |
|  | Lainnya |

Kategori kustom (buatan pengguna) direncanakan untuk versi berikutnya.

### Halaman riwayat transaksi

Halaman ini menampilkan seluruh transaksi pengguna, dengan contoh tampilan berikut:

| Tanggal | Kategori | Deskripsi | Jenis | Nominal |
| --- | --- | --- | --- | --: |
| 30/09/2026 | Makanan | Makan siang | Expense | Rp25.000 |
| 29/09/2026 | Transportasi | Bensin | Expense | Rp50.000 |
| 28/09/2026 | Gaji | Gaji bulanan | Income | Rp3.000.000 |

Fitur di halaman ini: pencarian, filter jenis transaksi, filter kategori, filter tanggal, edit, dan hapus.

## 7. Alur Pengguna dan Peta Halaman

&#91;embedded content: alur pengguna dan peta halaman · 10 halaman\]

Pengguna masuk lewat login atau register, lalu semua fitur diakses dari dashboard. Selain `/transactions`, halaman transaksi memiliki `/transactions/create` untuk menambah dan `/transactions/edit/:id` untuk mengubah data.

## 8. Desain Database

Database terdiri dari tiga tabel. Setiap data terikat ke pemiliknya lewat `user_id`, sehingga data antar-pengguna tidak tercampur.

### Users

| Kolom | Tipe | Keterangan |
| --- | --- | --- |
| id | INT | Primary key |
| name | VARCHAR | Nama pengguna |
| email | VARCHAR | Email pengguna |
| password | VARCHAR | Password (hash) |
| created\_at | DATETIME | Waktu akun dibuat |

### Categories

| Kolom | Tipe | Keterangan |
| --- | --- | --- |
| id | INT | Primary key |
| user\_id | INT | Pemilik kategori |
| name | VARCHAR | Nama kategori |
| type | ENUM | `income` atau `expense` |

### Transactions

| Kolom | Tipe | Keterangan |
| --- | --- | --- |
| id | INT | Primary key |
| user\_id | INT | Pemilik transaksi |
| category\_id | INT | Kategori transaksi |
| type | ENUM | `income` atau `expense` |
| amount | DECIMAL | Nominal transaksi |
| description | TEXT | Deskripsi transaksi |
| transaction\_date | DATE | Tanggal transaksi |
| created\_at | DATETIME | Waktu data dibuat |

### Relasi antar tabel

&#91;embedded content: relasi antar tabel · 3 tabel\]

Satu pengguna memiliki banyak kategori dan banyak transaksi, dan satu kategori dipakai oleh banyak transaksi.

## 9. Teknologi yang Digunakan

| Lapisan | Teknologi |
| --- | --- |
| Frontend | HTML5, CSS3, JavaScript, Bootstrap 5 |
| Backend | Python, Flask |
| Database | MySQL |
| Library | Flask-SQLAlchemy, Flask-Login, Werkzeug, Chart.js |

## 10. Kebutuhan Sistem

### Kebutuhan fungsional

| ID | Kebutuhan | Prioritas |
| --- | --- | --- |
| FR-01 | Pengguna dapat register | Must Have |
| FR-02 | Pengguna dapat login | Must Have |
| FR-03 | Pengguna dapat logout | Must Have |
| FR-04 | Pengguna dapat melihat dashboard | Must Have |
| FR-05 | Pengguna dapat menambahkan transaksi | Must Have |
| FR-06 | Pengguna dapat melihat transaksi | Must Have |
| FR-07 | Pengguna dapat mengedit transaksi | Must Have |
| FR-08 | Pengguna dapat menghapus transaksi | Must Have |
| FR-09 | Sistem menghitung saldo otomatis | Must Have |
| FR-10 | Pengguna dapat menggunakan kategori transaksi | Must Have |
| FR-11 | Pengguna dapat memfilter transaksi | Should Have |
| FR-12 | Pengguna dapat melihat laporan keuangan | Should Have |
| FR-13 | Pengguna dapat melihat grafik keuangan | Should Have |
| FR-14 | Pengguna dapat mengelola profil | Should Have |

### Kebutuhan non-fungsional

| Aspek | Persyaratan |
| --- | --- |
| Keamanan | Password disimpan dalam bentuk hash; pengguna hanya dapat mengakses data miliknya; endpoint yang butuh autentikasi harus dilindungi |
| Performa | Transaksi diproses tanpa delay berarti; query database dibuat efisien |
| Kemudahan penggunaan | Antarmuka sederhana, navigasi mudah dipahami, form transaksi ringkas |
| Responsive | Dapat digunakan di desktop, laptop, tablet, dan smartphone |
| Keandalan | Data transaksi tersimpan konsisten dan tidak berubah tanpa tindakan pengguna |

## 11. Cakupan MVP dan Fitur Masa Depan

### Termasuk dalam MVP

- [ ] Register, login, dan logout
- [ ] Dashboard
- [ ] Tambah, lihat, edit, dan hapus transaksi
- [ ] Kategori transaksi
- [ ] Perhitungan saldo otomatis
- [ ] Filter transaksi
- [ ] Laporan keuangan
- [ ] Profil pengguna

### Rencana setelah MVP

- [ ] Export laporan ke PDF dan Excel
- [ ] Custom category
- [ ] Budget management dan notifikasi pengeluaran
- [ ] Recurring transaction dan pengingat tagihan
- [ ] Integrasi e-wallet dan rekening bank
- [ ] AI financial assistant dan prediksi pengeluaran

## 12. Kriteria Penerimaan dan Metrik Keberhasilan

MVP dinyatakan memenuhi kebutuhan jika semua kriteria berikut terpenuhi.

### Kriteria penerimaan

**Autentikasi**

- [ ] Pengguna dapat membuat akun, login, dan logout.
- [ ] Password tidak disimpan sebagai plaintext.

**Transaksi**

- [ ] Pengguna dapat menambahkan pemasukan dan pengeluaran.
- [ ] Pengguna dapat melihat, mengedit, dan menghapus transaksi.
- [ ] Setiap transaksi memiliki kategori.

**Saldo**

- [ ] Sistem menghitung total pemasukan, total pengeluaran, dan saldo secara otomatis.
- [ ] Saldo berubah setelah transaksi ditambah, diubah, atau dihapus.

**Laporan**

- [ ] Pengguna dapat melihat laporan dan memfilternya berdasarkan periode.
- [ ] Sistem menampilkan ringkasan pemasukan dan pengeluaran.

**Data pengguna**

- [ ] Pengguna hanya dapat melihat transaksi miliknya.
- [ ] Data antar-pengguna tidak tercampur.

### Metrik keberhasilan

1. Seluruh fungsi CRUD transaksi berjalan.
2. Perhitungan saldo sesuai dengan transaksi yang tercatat.
3. Pengguna dapat mencatat transaksi tanpa error.
4. Data transaksi tersimpan dengan benar di database.
5. Sistem autentikasi berjalan dengan baik.
6. Dashboard menampilkan data sesuai transaksi pengguna.

## 13. Roadmap Pengembangan

&#91;embedded content: roadmap pengembangan · 8 fase\]

Fase dikerjakan berurutan dari kiri ke kanan, baris demi baris. Fase Testing mencakup pengujian autentikasi, CRUD, perhitungan saldo, database, dan responsive sebelum aplikasi di-deploy.

## 14. Repository, Issue, dan Definition of Done

### Struktur repository GitHub

```text
personal-finance/
├── app/
│   ├── __init__.py
│   ├── models.py
│   ├── routes.py
│   ├── templates/
│   │   ├── base.html
│   │   ├── login.html
│   │   ├── register.html
│   │   ├── dashboard.html
│   │   ├── transactions.html
│   │   ├── transaction_form.html
│   │   ├── reports.html
│   │   └── profile.html
│   └── static/
│       ├── css/style.css
│       └── js/script.js
├── migrations/
├── tests/
│   ├── test_auth.py
│   ├── test_transactions.py
│   └── test_dashboard.py
├── .env.example
├── .gitignore
├── config.py
├── requirements.txt
├── run.py
├── README.md
└── PRD.md
```

### Issue GitHub yang disarankan

| # | Issue | # | Issue |
| --- | --- | --- | --- |
| 1 | Setup Flask Project | 9 | Create Financial Reports |
| 2 | Setup Database | 10 | Create Transaction Filters |
| 3 | Create User Authentication | 11 | Create User Profile |
| 4 | Create User Model | 12 | Improve Responsive UI |
| 5 | Create Transaction Model | 13 | Add Form Validation |
| 6 | Create Category Model | 14 | Add Error Handling |
| 7 | Create Transaction CRUD | 15 | Testing |
| 8 | Create Dashboard | 16 | Deployment |

### Definition of Done

Sebuah fitur dianggap selesai jika:

- [ ] Fitur sudah diimplementasikan dan terhubung ke database bila perlu.
- [ ] Validasi input dan error handling sudah dibuat.
- [ ] Tampilan responsive.
- [ ] Fitur sudah diuji dan tidak ada bug utama.
- [ ] Kode sudah di-commit ke GitHub.
- [ ] Dokumentasi fitur sudah diperbarui.
