Nama:Mahendro Hamonangan Putra Manihuruk 

NPM:4525210093 

MataKuliah:PRAK.DesainWeb 

PERTEMUAN 2: 

# **1. Penjelasan Struktur HTML** 

- **Header dan Navigasi (<header> dan <nav>)** : Bagian atas halaman yang memiliki menu navigasi (Profil, Organisasi, Kontak). Menu ini menggunakan _anchor link_ (seperti href="#Profil") yang berfungsi untuk menggulirkan (scroll) halaman langsung ke bagian yang diklik. 

- **Bagian Profil (<section id="Profil">)** : Berisi penjelasan tentang fasilitas kampus, seperti Gedung Rektorat dan Gedung Fakultas Teknik. Bagian ini menampilkan gambar menggunakan tag <img> beserta teks penjelasannya. 

- **Bagian Organisasi (<section id="Organisasi">)** : Menampilkan daftar organisasi mahasiswa di Fakultas Teknik, yaitu BPM FT-KMUP, SEMA FT-KMUP, dan IMATIKA FT-KMUP. Setiap organisasi dijelaskan peranannya dan dilengkapi dengan logo masing-masing. 

- **Bagian Kontak (<section id="Kontak">)** : Menampilkan informasi alamat email dan tautan langsung (link) ke halaman Instagram masing-masing organisasi menggunakan tag <a>. Di bagian bawah terdapat tautan "kembali ke atas" yang mengarah ke id #Beranda. 

# **2. Penjelasan Desain CSS (Style.css)** 

- **body** : Mengatur jenis huruf (font) untuk seluruh halaman menjadi Arial (atau sans-serif) dan memberikan jarak tepi luar (margin) sebesar 75px di semua sisi. 

- **h1 dan h2** : Mengatur warna untuk judul utama. Judul h1 diubah menjadi warna biru (rgb(0, 0, 255)), sedangkan judul h2 diubah menjadi warna merah (rgb(255, 0, 0)). 

- **img** : Membuat sudut dari setiap gambar menjadi sedikit melengkung dengan menambahkan efek border-radius: 10px. 

- **.daftar-keahlian** : Mengatur jarak antar baris (line-height) menjadi 1.8, meskipun _class_ ini tidak digunakan pada file HTML di atas. 

- **a dan a:hover** : Menghilangkan garis bawah default pada semua tautan teks (text-decoration: none;). Garis bawah baru akan muncul hanya ketika kursor _mouse_ diarahkan ke atas tautan tersebut (a:hover). 

