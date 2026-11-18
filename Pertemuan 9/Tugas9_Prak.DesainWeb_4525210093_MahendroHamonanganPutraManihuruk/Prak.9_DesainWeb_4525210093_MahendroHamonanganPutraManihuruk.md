Nama:Mahendro Hamonangan Putra Manihuruk 

NPM:4525210093 

MataKuliah:PRAK.DesainWeb 

# **PERTEMUAN 9:** 

# **A. Fungsi container, row, dan column pada Halaman** 

Tata letak halaman dashboard ini dibangun menggunakan tiga lapisan grid Bootstrap yang saling bersarang: 

   1. **container** : Berfungsi sebagai pembungkus utama pada bagian <header>, <main>, dan <footer> untuk membatasi lebar maksimal konten agar tidak melebar penuh ke ujung layar monitor besar, sekaligus memosisikan seluruh isi halaman secara simetris di tengah ( _center_ ) dengan _padding_ kiri-kanan otomatis. 

   2. **row** : Digunakan di dalam <section> statistik untuk mengelompokkan keempat kartu secara horizontal dalam satu baris sistem 12 kolom. Class tambahan g-3 ( _gutter_ ) memberikan jarak antar-kartu baik secara horizontal maupun vertikal saat kartu bertumpuk di layar kecil. 

   3. **column (col-12 col-md-6 col-lg-3)** : Berfungsi sebagai unit tata letak di dalam row yang mengatur proporsi lebar masing-masing kartu berdasarkan _breakpoint_ ukuran layar: 

      - **Layar HP (< 768px)** : Class col-12 aktif sehingga setiap kartu mengambil seluruh 12 kolom ( **1 kolom per baris** / lebar penuh). 

      - **Layar Tablet (≥ 768px)** : Class col-md-6 aktif sehingga setiap kartu mengambil 6 dari 12 kolom ( **2 kolom per baris** ). 

      - **Layar Laptop/Desktop (≥ 1024px / lg)** : Class col-lg-3 aktif sehingga setiap kartu mengambil 3 dari 12 kolom ( **4 kolom sejajar dalam 1 baris** ). 

- **B. Penjelasan Komponen & Utility Classes yang Digunakan** 

   - **Utility Classes** : 

      - **Warna latar & teks** : bg-primary, bg-light, bg-white, text-white, textsecondary, text-success, text-warning untuk hierarki visual informasi. 

      - **Jarak (** **_Spacing_ )** : py-4, mb-4, mb-5, ps-3, pe-3 untuk mengatur ruang napas ( _padding_ dan _margin_ ) antar-elemen tanpa menulis CSS manual. 

      - **Bayangan & Perataan** : shadow-sm pada header dan kartu untuk efek elevasi tipis, serta text-center pada kolom aksi dan footer. 

   - **Tabel Responsif & Pelengkap** : 

      - table, table-striped, dan table-hover memberikan warna baris selangseling serta sorotan interaktif saat kursor diarahkan ke baris data mahasiswa. 

      - table-responsive membungkus elemen <table> agar muncul _horizontal scrollbar_ ketika dibuka di layar HP. 

      - **Badge (badge rounded-pill text-bg-*)** membedakan status mahasiswa secara visual ( _Aktif_ hijau, _Cuti_ kuning, _Nonaktif_ merah, _Yudisium_ biru muda). 

      - **Button (btn btn-primary btn-sm dan btn-outline-primary btn-sm)** digunakan untuk tombol tambah data di bagian atas tabel dan tombol aksi _Detail_ pada setiap baris. 

- **C. Masalah yang Ditemui dan Solusinya** 

   1. **Masalah 1 — Teks Kolom Tabel Menumpuk dan Memanjang ke Bawah di Layar HP** : 

      - _Penyebab_ : Ketika dibuka pada resolusi mobile (< 576px), kolom seperti "Nama Mahasiswa" dan "Program Studi" otomatis turun baris ( _text wrapping_ ), membuat tinggi setiap baris tabel menjadi tidak seragam dan sulit dibaca. 

      - _Solusi_ : Membungkus <table> dengan <div class="table-responsive"> dari Bootstrap dan menambahkan aturan white-space: nowrap; pada sel tabel di css/style.css. Hasilnya, tabel tetap rapi dalam satu baris per data dan dapat digeser ke samping ( _horizontal scroll_ ) dengan mulus di layar ponsel. 

   2. **Masalah 2 — Tinggi Kartu Statistik Tidak Sama saat Teks Keterangan Berbeda Panjang** : 

      - _Penyebab_ : Pada tampilan tablet (2 kolom) atau desktop (4 kolom), kartu yang memiliki teks keterangan lebih panjang terlihat lebih tinggi dibanding kartu di sebelahnya. 

      - _Solusi_ : Menambahkan utility class h-100 (height: 100%) pada setiap elemen <div class="card"> di dalam kolom grid sehingga tinggi keempat kartu otomatis sejajar. 

   3. **Masalah 3 — Header Tabel Terlihat Bertabrakan di Layar Kecil** : 

      - _Penyebab_ : Judul tabel dan tombol + Tambah Data Mahasiswa berada dalam satu baris sempit pada layar ponsel. 

- _Solusi_ : Menggunakan utility flex responsif d-flex flex-column flex-sm-row justify-content-between gap-2 pada card-header sehingga tombol otomatis turun ke bawah judul saat di layar HP dan kembali sejajar kanan-kiri pada layar tablet maupun laptop. 

