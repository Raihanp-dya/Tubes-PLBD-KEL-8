# LAPORAN TUGAS BESAR PEMROGRAMAN LANJUT

> [Gambar: Logo Institut Teknologi Kalimantan]

# [JUDUL TUGAS BESAR/FINAL PROJECT]

Kelompok 8:

- Raihan Pramudya 10251099
- Muhammad Rizqi Akbar 10251074
- Shiva Andriyana 10251024

PROGRAM STUDI SISTEM INFORMASI  
JURUSAN TEKNIK ELEKTRO, INFORMATIKA, DAN BISNIS  
FAKULTAS SAINS DAN TEKNOLOGI INFORMASI  
BALIKPAPAN  
2026

---

## DAFTAR ISI

- BAB I PENDAHULUAN ................................................................................................ 4
  - 1.1. Judul ................................................................................................................ 4
  - 1.2. Latar Belakang ................................................................................................ 4
  - 1.3. Tujuan Pembuatan Aplikasi ............................................................................. 5
- BAB II METODE PENELITIAN ................................................................................... 6
  - 2.1. Diagram Alir Penelitian .................................................................................. 6
  - 2.2. Planning ........................................................................................................... 7
  - 2.3. Design .............................................................................................................. 9
    - 2.3.1. Entity Relationship Diagram ..................................................................... 9
    - 2.3.2. Class Diagram ............................................................................................ 9
  - 2.4. Development ..................................................................................................... 9
- BAB III HASIL DAN PEMBAHASAN ........................................................................ 11
  - 3.1. Hasil Development .......................................................................................... 11
    - 3.1.1. Struktur Provek dan Arsitektur MVC ...................................................... 11
    - 3.1.2. Implementasi PDO (PHP Data Objects) .................................................. 11
    - 3.1.3. Implementasi Query Builder Database .................................................... 11
    - 3.1.4. Implementasi OOP (Object-Oriented Programming) .............................. 12
    - 3.1.5. Implementasi Validasi Data ..................................................................... 12
  - 3.2. Analisis Fitur Utama ....................................................................................... 12
    - 3.2.1. Fitur 1 ....................................................................................................... 12
    - 3.2.2. Fitur 2 dst ................................................................................................. 13
  - 3.3. Pengujian Sistem ............................................................................................. 13
    - 3.3.1. Hasil Uji Create ......................................................................................... 13
    - 3.3.2. Hasil Uji Read ........................................................................................... 13
    - 3.3.3. Hasil Uji Update ........................................................................................ 13
    - 3.3.4. Hasil Uji Delete .......................................................................................... 14
    - 3.3.5. Hasil Uji lainnya ........................................................................................ 14
- BAB IV ....................................................................................................................... 15
- PENUTUP ................................................................................................................... 15
  - 4.1. Kesimpulan ...................................................................................................... 15
  - 4.2. Saran ................................................................................................................ 15
- DAFTAR PUSTAKA .................................................................................................... 16
- LAMPIRAN ................................................................................................................ 17

---

## RINGKASAN

Tuliskan ringkasan setelah seluruh bab selesai dikerjakan, dalam satu paragraf sepanjang 150–250 kata. Ringkasan memuat: masalah yang melatarbelakangi pembuatan aplikasi, tujuan aplikasi, metode pengembangan yang digunakan (misalnya Extreme Programming), teknologi utama (PHP, arsitektur MVC, PDO, MySQL), fitur-fitur utama yang berhasil dibangun, serta hasil pengujian secara singkat. Hindari menulis kutipan, gambar, atau potongan kode di bagian ini.

**Kata Kunci:** Tuliskan 3–5 kata kunci yang mewakili isi laporan, dipisahkan tanda titik koma dan diurutkan sesuai abjad. Contoh: MVC; OOP; PDO; PHP; Sistem Informasi Inventaris.

---

## BAB I PENDAHULUAN

## 1.1. Judul

Judul Aplikasi adalah Sistem Informasi Manajemen Stok dan Transaksi Penjualan Berbasis Web pada Toko Bangunan TB Alya Menggunakan Arsitektur MVC dan Query Builder. Aplikasi yang Dibangun adalah sistem informasi berbasis web yang berfokus pada pengelolaan inventaris barang (inventory management), pencatatan transaksi barang masuk dari supplier, transaksi penjualan ke pelanggan, serta pembuatan laporan secara otomatis. Pengguna atau Organisasi Sasaran ditujukan untuk operasional internal Toko Bangunan TB Alya, khususnya bagi pemilik toko (owner) dalam memantau ketersediaan stok dan laporan keuangan, serta bagian kasir/admin dalam melayani transaksi harian. Masalah yang Ingin Diselesaikan Mengatasi kelemahan sistem pencatatan manual menggunakan berkas kertas, ketiadaan nomor nota unik yang menyulitkan pencarian riwayat transaksi, risiko hilangnya nota pembelian dari supplier, serta ketidaksinkronan antara jumlah stok fisik dan catatan akibat tidak adanya pengurangan stok otomatis saat terjadi penjualan.

## 1.2. Latar Belakang

Toko Bangunan TB Alya merupakan usaha yang bergerak di bidang penjualan material bangunan seperti semen, pasir, bata merah, besi, cat, pipa, dan baut. Dalam kegiatan sehari-hari, toko mencatat barang masuk dari supplier dan barang keluar melalui penjualan menggunakan berkas kertas. Nota penjualan memuat nama barang, tanggal, harga satuan, jumlah, dan total, tetapi tidak memiliki nomor nota unik serta tidak mencantumkan identitas pembeli. Nota dari supplier juga disimpan dalam bentuk kertas dan formatnya bervariasi antar supplier.

Pencatatan manual tersebut menimbulkan beberapa masalah. Pemilik (owner) sulit memantau stok barang secara real-time, riwayat transaksi sulit dicari, dan laporan penjualan maupun stok harus dihitung ulang secara manual. Stok juga tidak berkurang otomatis ketika terjadi penjualan, sehingga sering terjadi selisih antara catatan dan kondisi fisik barang. Selain itu, data barang masuk dari supplier hanya dicatat di kertas sehingga rawan hilang.

## 1.3. Tujuan Pembuatan Aplikasi

Tujuan pembuatan aplikasi pengelolaan data pada Toko Bangunan TB Alya adalah sebagai berikut:

- Mempermudah proses pencatatan dan pengelolaan data barang, meliputi nama barang, merek, kategori, satuan, harga beli, harga jual, dan jumlah stok.
- Mempermudah pencatatan transaksi penjualan beserta rincian barang yang dijual sehingga riwayat transaksi dapat tersimpan dengan terstruktur.
- Mempermudah pencatatan transaksi pembelian barang dari supplier beserta informasi barang yang diterima.
- Membantu pemilik toko dalam memantau persediaan stok barang berdasarkan kategori dan satuan.
- Mempermudah penyajian informasi dan laporan penjualan, pembelian, serta persediaan barang melalui pengolahan data pada basis data.
- Mengurangi ketergantungan terhadap pencatatan manual menggunakan kertas dan nota sehingga pengelolaan informasi menjadi lebih efektif dan terorganisir.

---

## BAB II METODE PENELITIAN

## 2.1. Diagram Alir Penelitian

## 2.1.1. Kompleksitas Basis Data dan Logika OOP

Proyek ini melibatkan relasi database yang cukup banyak (Tabel supplier, Barang, Transaksi Penjualan, Detail penjualan, dll.) serta logika pemrograman yang berorientasi objek untuk pemotongan stok otomatis.

## 2.1.2. Masalah Nyata

Masalah utama di Toko Bangunan TB Alya adalah pencatatan manual dan stok yang sering tidak sinkron. Dengan pendekatan prototyping, antarmuka kasir dan pencatatan nota unik dapat divisualisasikan lebih awal untuk memastikan alur transaksinya sudah logis dan solutif.

## 2.1.3. Metode yang dipilih

Dengan pertimbangkan Kompleksitas Basis Data, Logika OOP dan Masalah nyata dipilih metode Prototyping yang bisa membangun bentuk dasar (prototype) sistem dan struktur datanya terlebih dahulu, lalu mengujinya secara bertahap sebelum membangun seluruh fitur yang rumit.

## 2.1.4. Diagram Alur Prototype

> [Gambar: Diagram Alur Prototype]

## 2.1.5. Penjelasan Tahapan Metode Prototyping

1. **Pengumpulan Kebutuhan & Analisis Masalah (Requirement Collection):**  
   Mengkaji permasalahan nyata di Toko Bangunan TB Alya, seperti pencatatan manual dengan berkas kertas, nota tanpa nomor unik, dan stok barang yang tidak berkurang otomatis.

2. **Membangun Prototype Awal (Build Prototype):**  
   Membuat rancangan dasar (mockup antarmuka sederhana) serta perancangan basis data relasional (ERD) untuk tabel Barang, Supplier, dan Transaksi.

3. **Evaluasi Prototype (Evaluation):**  
   Meninjau apakah rancangan awal sudah dapat menjawab masalah utama toko (misalnya, apakah alur input penjualan sudah bisa memotong stok). Jika ada kekurangan, dilakukan perbaikan desain.

4. **Implementasi / Pengkodean Sistem (Coding / Implementation):**  
   Setelah purwarupa disetujui, tahap pengkodean sesungguhnya dilakukan menggunakan PHP OOP, arsitektur MVC, dan pemanfaatan Query Builder untuk menghubungkan aplikasi dengan database MySQL.

5. **Pengujian Sistem (Testing):**  
   Menguji fungsionalitas aplikasi secara menyeluruh (misalnya menggunakan Black-Box Testing) untuk memastikan seluruh fitur khususnya pengurangan stok otomatis dan pencarian nota berjalan tanpa bug.

6. **Sistem Selesai (Deployment/Use):**  
   Aplikasi siap digunakan oleh pengguna di Toko Bangunan TB Alya dan siap untuk didemonstrasikan dalam sidang Tugas Besar.

## 2.2. Planning

### 2.2.1. Identifikasi Kebutuhan Pengguna

Berdasarkan hasil wawancara dan observasi, kebutuhan utama pengguna adalah:

1. Pencatatan penjualan dan pembelian tidak lagi manual.
2. Stok barang dapat dipantau dan diperbarui setelah transaksi.
3. Data barang memiliki kategori, merek, satuan, harga beli, harga jual, dan stok.
4. Nota penjualan dan pembelian memiliki identitas transaksi yang unik.
5. Laporan penjualan, pembelian, dan stok dapat ditampilkan dengan cepat.

### 2.2.2. Daftar Kebutuhan Fungsional

1. Login dan logout.
2. CRUD kategori.
3. CRUD barang.
4. Transaksi penjualan beserta detail penjualan.
5. Transaksi pembelian beserta detail pembelian.
6. Pengurangan stok otomatis pada penjualan.
7. Penambahan stok otomatis pada pembelian.
8. Laporan stok, penjualan, pembelian, dan barang terlaris.

### 2.2.3. Kebutuhan Non-Fungsional

| Kebutuhan Non-Fungsional | Keterangan |
|---|---|
| Keamanan | Password disimpan menggunakan `password_hash()`, query menggunakan PDO prepared statement |
| Kemudahan penggunaan | Antarmuka sederhana, navigasi jelas, dan nota transaksi mudah dipahami. |
| Kinerja |  |
| Maintainability | Kode menggunakan MVC, OOP, dan pemisahan folder model, controller, view. |
| Kompatibilitas |  |

### 2.2.4. Aktor atau Peran Pengguna Beserta Hak Aksesnya

| Aktor | Hak Akses |
|---|---|
| Owner | Dashboard, CRUD kategori, CRUD barang, transaksi penjualan, transaksi pembelian, laporan, login, logout. |
| Karyawan | Dashboard, transaksi penjualan, transaksi pembelian, melihat stok, login, logout. |

### 2.2.5. Perangkat Lunak dan Perangkat Keras Yang Digunakan

| Komponen | Keterangan |
|---|---|
| Bahasa Pemrograman | PHP 8.x, CSS |
| Arsitektur | MVC |
| Database | MySQL -.-.- |
| DBMS/Tools | Laragon, phpMyAdmin, VS Code |
| Version Control | Git/GitHub |
| Browser | Chrome/Firefox |
| Sistem Operasi | Windows/Linux |

## 2.3. Design (belum di isi kebawah)

Jelaskan rancangan sistem yang dibuat sebelum masuk ke tahap pengkodean. Bagian ini berisi gambaran umum rancangan basis data dan struktur kelas program yang dirinci pada subbab berikut. Bila ada, tambahkan rancangan antarmuka (mockup atau wireframe) halaman-halaman utama aplikasi.

## 2.3.1. Entity Relationship Diagram

Tampilkan Entity Relationship Diagram (ERD) dari basis data aplikasi lengkap dengan nomor dan keterangan gambar. Jelaskan setiap entitas (tabel) beserta atribut, primary key, dan foreign key, kemudian jelaskan relasi antarentitas dan kardinalitasnya (one-to-one, one-to-many, atau many-to-many). Pastikan ERD sesuai dengan tabel yang benar-benar dibuat di database aplikasi.

## 2.3.2. Class Diagram

Tampilkan Class Diagram yang menggambarkan kelas-kelas dalam aplikasi, terutama kelas Model, Controller, dan kelas pendukung seperti kelas koneksi database atau Query Builder. Untuk setiap kelas, cantumkan atribut dan method beserta visibilitasnya (public, private, protected). Jelaskan hubungan antarkelas, misalnya pewarisan (inheritance) dari kelas induk seperti BaseModel atau BaseController, asosiasi, atau dependensi.

## 2.4. Development

Jelaskan proses pengkodean aplikasi berdasarkan rancangan yang telah dibuat. Uraikan urutan pengerjaan (misalnya membuat struktur folder, koneksi database, model, controller, lalu view), alat bantu yang digunakan (text editor, Git/GitHub untuk version control, XAMPP/Laragon), serta kendala yang ditemui selama pengembangan dan cara mengatasinya. Pembahasan rinci hasil kode ditulis di Bab III.

---

## BAB III HASIL DAN PEMBAHASAN

## 3.1. Hasil Development

Jelaskan secara umum hasil pengembangan aplikasi: teknologi yang digunakan, gambaran alur kerja aplikasi, dan bagian-bagian implementasi teknis yang dibahas pada subbab berikut. Setiap potongan kode yang ditampilkan harus diberi nomor dan keterangan (contoh: Kode 3.1 Kelas Database), cukup bagian pentingnya saja, lalu dijelaskan maksud dan cara kerjanya.

## 3.1.1. Struktur Provek dan Arsitektur MVC

Tampilkan struktur folder proyek (dalam bentuk tangkapan layar atau tree), lalu jelaskan fungsi setiap folder dan file utama, misalnya folder `app/models`, `app/controllers`, `app/views`, `config`, dan `public`. Jelaskan bagaimana arsitektur MVC diterapkan: peran Model dalam mengelola data, View dalam menampilkan antarmuka, dan Controller sebagai penghubung keduanya. Jelaskan juga alur sebuah request dari pengguna, mulai dari routing, diproses Controller, mengambil data lewat Model, hingga ditampilkan oleh View.

## 3.1.2. Implementasi PDO (PHP Data Objects)

Tampilkan potongan kode koneksi database menggunakan PDO, lalu jelaskan konfigurasi yang digunakan (DSN, username, password, dan opsi seperti `PDO::ATTR_ERRMODE`). Jelaskan penggunaan prepared statement dan binding parameter untuk mencegah SQL Injection, serta cara penanganan error menggunakan try-catch (`PDOException`). Berikan contoh penggunaannya pada salah satu proses di aplikasi.

## 3.1.3. Implementasi Query Builder Database

Jelaskan kelas atau method Query Builder yang dibuat untuk menyusun query secara dinamis, misalnya method `select()`, `where()`, `insert()`, `update()`, `delete()`, dan `orderBy()`. Tampilkan potongan kodenya dan contoh pemanggilannya di Model, lalu jelaskan bagaimana Query Builder mengubah pemanggilan method tersebut menjadi perintah SQL. Jelaskan juga keuntungan penggunaannya dibandingkan menulis query SQL secara langsung di setiap bagian kode.

## 3.1.4. Implementasi OOP (Object-Oriented Programming)

Jelaskan penerapan konsep OOP dalam aplikasi disertai potongan kode untuk setiap konsep: class dan object, encapsulation (penggunaan access modifier serta getter dan setter), inheritance (misalnya Model turunan dari kelas induk), polymorphism (method overriding atau interface), dan abstraction (abstract class atau interface). Jika menggunakan namespace atau autoloading, jelaskan juga. Tunjukkan di bagian mana saja setiap konsep diterapkan dan apa manfaatnya bagi aplikasi.

## 3.1.5. Implementasi Validasi Data

Jelaskan mekanisme validasi data yang diterapkan sebelum data disimpan ke database, misalnya validasi field wajib diisi, format email, panjang karakter, tipe angka, dan data unik. Tampilkan potongan kode validasi (fungsi atau kelas Validator) dan jelaskan di mana validasi dijalankan (sisi server di Controller atau Model, dan bila ada di sisi klien). Jelaskan juga cara menampilkan pesan error kepada pengguna serta upaya sanitasi input untuk mencegah XSS.

## 3.2. Analisis Fitur Utama

Jelaskan daftar fitur utama aplikasi secara singkat, lalu bahas setiap fitur pada subbab tersendiri. Urutkan fitur berdasarkan alur penggunaan aplikasi atau berdasarkan tingkat kepentingannya.

## 3.2.1. Fitur 1

Tuliskan nama fitur sebagai judul subbab ini. Tampilkan tangkapan layar antarmuka fitur dengan nomor dan keterangan gambar, lalu jelaskan fungsi fitur, siapa pengguna yang dapat mengaksesnya, langkah penggunaannya, dan alur proses di baliknya (Controller dan Model yang terlibat). Bila perlu, sertakan potongan kode yang paling penting dari fitur tersebut.

## 3.2.2. Fitur 2 dst

Ulangi format yang sama seperti Fitur 1 untuk fitur-fitur berikutnya. Ganti judul subbab dengan nama fitur dan tambahkan subbab baru sesuai jumlah fitur utama aplikasi.

## 3.3. Pengujian Sistem

Jelaskan metode pengujian yang digunakan, misalnya Black Box Testing, beserta lingkungan pengujiannya (browser, sistem operasi, versi PHP dan database). Hasil pengujian setiap operasi disajikan dalam bentuk tabel dengan kolom: No, Skenario Pengujian, Data Uji, Hasil yang Diharapkan, Hasil Aktual, dan Status (Berhasil/Gagal). Uji tidak hanya kondisi normal, tetapi juga kondisi salah seperti input kosong atau format tidak sesuai.

## 3.3.1. Hasil Uji Create

Sajikan tabel hasil pengujian proses menambah data (Create), termasuk skenario input valid dan input tidak valid untuk menguji validasi. Lampirkan tangkapan layar form input, pesan berhasil atau pesan error, serta bukti data tersimpan di database, lalu jelaskan hasilnya.

## 3.3.2. Hasil Uji Read

Sajikan tabel hasil pengujian proses menampilkan data (Read), misalnya menampilkan daftar data, detail data, pencarian, filter, atau pagination. Lampirkan tangkapan layar hasilnya dan pastikan data yang tampil sesuai dengan isi database.

## 3.3.3. Hasil Uji Update

Sajikan tabel hasil pengujian proses mengubah data (Update), termasuk skenario data valid dan tidak valid. Lampirkan tangkapan layar sebelum dan sesudah data diubah, lalu jelaskan apakah perubahan tersimpan dengan benar di database.

## 3.3.4. Hasil Uji Delete

Sajikan tabel hasil pengujian proses menghapus data (Delete), termasuk konfirmasi sebelum penghapusan dan perilaku sistem jika data masih berelasi dengan tabel lain. Lampirkan tangkapan layar sebelum dan sesudah penghapusan, lalu jelaskan hasilnya.

## 3.3.5. Hasil Uji lainnya

Sajikan hasil pengujian fitur lain di luar CRUD, misalnya login dan logout, pembatasan hak akses berdasarkan peran pengguna, upload file, export laporan, atau fitur khusus aplikasi kalian. Gunakan format tabel yang sama dan jelaskan hasilnya. Jika tidak ada pengujian tambahan, subbab ini boleh dihapus.

---

## BAB IV

## PENUTUP

## 4.1. Kesimpulan

Tuliskan kesimpulan yang menjawab setiap tujuan pembuatan aplikasi pada subbab 1.3, sebaiknya dalam bentuk poin dengan urutan yang sama. Kesimpulan didasarkan pada hasil implementasi dan pengujian di Bab III, bukan mengulang teori. Contoh: Aplikasi berhasil dibangun dengan arsitektur MVC dan seluruh fitur CRUD berjalan sesuai skenario pengujian.

## 4.2. Saran

Tuliskan saran untuk pengembangan aplikasi selanjutnya berdasarkan keterbatasan yang ditemukan selama pengerjaan, misalnya penambahan fitur, peningkatan keamanan, perbaikan tampilan, pembuatan versi mobile, atau integrasi dengan sistem lain. Saran harus realistis dan berkaitan dengan aplikasi yang dibuat.

---

## DAFTAR PUSTAKA

Tuliskan seluruh sumber yang dirujuk dalam laporan (jurnal, buku, dokumentasi resmi PHP, artikel ilmiah) menggunakan gaya sitasi yang konsisten, misalnya APA atau IEEE. Urutkan sesuai abjad (APA) atau sesuai urutan kemunculan sitasi (IEEE). Hanya cantumkan sumber yang benar-benar dikutip di dalam isi laporan.

---

## LAMPIRAN

Lampirkan bahan pendukung yang tidak dimasukkan ke dalam isi laporan, misalnya tautan repository GitHub proyek, tautan video demo aplikasi, dump struktur database (file `.sql`), tangkapan layar tambahan, user manual singkat, dan bukti pembagian tugas kelompok. Beri judul dan nomor pada setiap lampiran (contoh: Lampiran 1 Tautan Repository).