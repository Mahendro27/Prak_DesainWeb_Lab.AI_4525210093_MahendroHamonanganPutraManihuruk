Nama:Mahendro Hamonangan Putra Manihuruk 

NPM:4525210093 

MataKuliah:PRAK.DesainWeb 

**PERTEMUAN 10:** 

# **A. Penjelasan Implementasi & Modifikasi CSS (Branding)** 

   1. **Urutan Pemanggilan CSS** : File CSS/style.css diletakkan setelah tautan CDN bootstrap.min.css di dalam <head> agar aturan gaya merek _Selaras Coffee_ dapat menimpa gaya bawaan Bootstrap secara bersih tanpa konflik. 

   2. **Design Tokens (:root)** : Variabel warna seperti --brand-primary (#4A2C2A) dan -- brand-accent (#C87D4B) disimpan di dalam :root sehingga identitas warna kedai kopi konsisten di seluruh komponen (tombol, navbar, alert, badge, modal, dan footer). 

   3. **Custom Class Tanpa !important** : Pembuatan class khusus seperti .customnavbar, .btn-brand, .btn-outline-brand, dan .custom-alert mencegah perubahan gaya merusak komponen Bootstrap lain serta memudahkan pemeliharaan kode. 

   4. **Responsivitas Mobile-First** : 

      - **Navbar** : Menggunakan navbar-expand-lg sehingga otomatis menyusut ( _collapse_ ) menjadi tombol _hamburger_ pada layar HP dan Tablet, lalu melebar horizontal pada layar Laptop (≥ 992px). 

      - **Grid Produk** : Menggunakan kombinasi col-12 col-md-6 col-lg-4 sehingga 3 kartu produk tampil bertumpuk **1 kolom di HP** , **2 kolom di Tablet** , dan **3 kolom sejajar di Laptop** . 

- **B. Masalah yang Ditemui dan Solusinya** 

   1. **Masalah 1 — Komponen Interaktif (Navbar Toggle, Alert Dismiss, Modal) Tidak Berfungsi** : 

      - _Penyebab_ : Komponen interaktif Bootstrap memerlukan skrip JavaScript agar atribut data-bs-toggle dan data-bs-dismiss berjalan. 

      - _Solusi_ : Menambahkan bootstrap.bundle.min.js di bagian bawah sebelum tag penutup </body>. 

   2. **Masalah 2 — Tinggi Gambar Kartu Produk Tidak Seragam** : 

      - _Penyebab_ : Rasio foto produk yang berbeda membuat ukuran kartu tidak sejajar saat ditampilkan 2 atau 3 kolom. 

   - _Solusi_ : Menambahkan class .product-img dengan tinggi tetap (height: 220px;) dan properti object-fit: cover; pada CSS/style.css, serta menambahkan class h-100 pada .card agar tinggi semua kartu rata. 

3. **Masalah 3 — Warna Teks Tombol Custom Kembali Menjadi Gelap saat Hover** : 

   - _Penyebab_ : Gaya :hover bawaan Bootstrap menimpa warna teks tombol kustom. 

   - _Solusi_ : Mendefinisikan state .btn-brand:hover dan .btn-outlinebrand:hover secara eksplisit di CSS/style.css dengan color: #f **f** ff;. 

