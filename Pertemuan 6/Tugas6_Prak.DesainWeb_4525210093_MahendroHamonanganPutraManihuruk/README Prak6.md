Nama:Mahendro Hamonangan Putra Manihuruk 

NPM:4525210093 

MataKuliah:PRAK.DesainWeb 

PERTEMUAN 6: 

# **1. Inkonsistensi Visual dan Nilai Absolut (Magic Numbers)** 

- **Masalah** : Menuliskan kode warna spesifik (seperti #c0281f) atau ukuran ukuran secara absolut secara berulang-ulang di berbagai elemen membuat desain rentan tidak konsisten dan menyulitkan pembaruan skala besar. 

- **Perubahan** : Diperkenalkannya _Design Tokens_ menggunakan CSS Variables (seperti --primary, --neutral-50, --radius-md, dan --space-1 hingga --space-6) yang dideklarasikan pada pseudo-class :root di dalam style_3.css. 

- **Solusi** : Variabel ini menstandarkan seluruh nilai desain. Jika ada _re-branding_ atau perubahan warna merek, pengembang hanya perlu mengubah satu baris kode di tingkat :root, dan seluruh situs akan otomatis menyesuaikan diri. 

# **2. Ketiadaan Panduan Referensi (Single Source of Truth)** 

- **Masalah** : Dalam pengembangan berkelanjutan, pengembang atau desainer sering kali kebingungan mencari gaya tombol, ukuran teks, atau bentuk kartu yang standar, sehingga sering menciptakan elemen baru yang membebani kinerja. 

- **Perubahan** : Dibuatnya berkas khusus dokumentasi design-system.html beserta gaya pelengkapnya di design-system.css. Berkas ini memuat katalog lengkap untuk warna, tipografi, jarak (spacing), tombol, kontrol formulir, dan kartu. 

- **Solusi** : Halaman ini bertindak sebagai "sumber kebenaran tunggal". Siapa pun yang bertugas mengembangkan halaman baru dapat melihat katalog ini, mengambil nama kelas yang sudah ada, dan menempelkannya, sehingga tampilan aplikasi selalu seragam tanpa harus menebak-nebak. 

# **3. Struktur Kode yang Sulit Didaur Ulang (Spaghetti Code)** 

- **Masalah** : HTML dan CSS yang ditulis terikat erat secara spesifik pada satu halaman akan sulit digunakan kembali pada halaman lain. 

- **Perubahan** : Penggunaan arsitektur kelas berbasis komponen (ComponentBased CSS) di index_3.html dan style_3.css. Contohnya adalah pemisahan kelas .container murni untuk pembatas tata letak, pola modifier .btn bersanding dengan .btn-primary, serta .feature-card untuk komponen konten. 

- **Solusi** : Elemen antarmuka menjadi sangat modular (dapat digunakan kembali). Tombol atau kartu dapat dipanggil berkali-kali di berbagai halaman hanya dengan menggunakan kelas penandanya, mempercepat waktu pengembangan dan menjaga CSS tetap ringan. 

# **4. Kerusakan Tata Letak pada Berbagai Layar Perangkat** 

- **Masalah** : Komponen yang dirancang berjejer untuk layar monitor (desktop) akan menumpuk, menyempit, atau terpotong ketika diakses melalui perangkat seluler. 

- **Perubahan** : Pengimplementasian modul _CSS Grid_ modern (seperti gridtemplate-columns: repeat(3, 1fr)) dipadukan dengan _Media Queries_ pada style_3.css yang mendeteksi batas lebar layar maksimum 900px dan 600px. 

- **Solusi** : Antarmuka menjadi sepenuhnya adaptif dan responsif. Tata letak pahlawan (Hero) maupun daftar menu yang awalnya memiliki tiga pilar akan otomatis direorganisasi menjadi dua pilar pada tablet (di bawah 900px) dan menjadi satu pilar menumpuk dari atas ke bawah pada layar ponsel (di bawah 600px). Hal ini memastikan semua konten tetap proporsional dan mudah dibaca tanpa harus di-zoom oleh pengguna. 

