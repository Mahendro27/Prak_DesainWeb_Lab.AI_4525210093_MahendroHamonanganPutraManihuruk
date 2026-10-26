Nama:Mahendro Hamonangan Putra Manihuruk 

NPM:4525210093 

MataKuliah:PRAK.DesainWeb 

PERTEMUAN 4: 

# **Struktur HTML** 

- **Navigasi Dalam Halaman (Anchor Links):** Bagian <header> berisi menu navigasi (Tentang, Proyek, Kontak) yang terhubung langsung dengan atribut id pada masing-masing <section> di bawahnya (misalnya, href="#tentang" akan menggulir ke <section id="tentang">). 

- **Pembagian Konten:** Area <main> dipecah menjadi empat bagian utama menggunakan tag <section>, yaitu: perkenalan diri (#hero), informasi pribadi (#tentang), daftar proyek (#proyek), dan informasi kontak (#kontak). 

- **Daftar Proyek:** Di dalam section proyek, terdapat kontainer div dengan kelas card-list yang membungkus tiga buah kartu (card), masing-masing menampilkan nama dan deskripsi singkat dari proyek yang pernah dikerjakan. 

- **Tombol Kembali ke Atas:** Pada bagian kontak, terdapat tautan dengan tautan href="#atas" yang akan membawa pengguna kembali ke elemen <body id="atas"> di bagian paling atas halaman. 

# **Gaya dan Tata Letak CSS** 

- **Efek Gulir Mulus (Smooth Scrolling):** Properti scroll-behavior: smooth diterapkan pada elemen html agar transisi perpindahan saat mengklik menu navigasi terasa halus. 

- **Header Menempel (Sticky Header):** Elemen header menggunakan properti position: sticky dengan top: 0, sehingga menu navigasi akan selalu tetap berada di bagian atas layar meskipun pengguna menggulir halaman ke bawah. 

- **Penggunaan Flexbox:** Properti display: flex digunakan untuk mengatur tata letak pada header (menyebarkan judul dan menu ke dua sisi) serta pada .card-list (menyusun kartu proyek secara sejajar horizontal). 

- **Efek Interaktif (Hover):** Elemen kartu (.card) diberikan efek bayangan (boxshadow) dan akan bergerak sedikit ke atas (transform: translateY(-5px)) saat disorot kursor, sementara tombol (.button) akan berubah warna latar belakangnya menjadi hijau (#2e7d32) saat disorot. 

- **Desain Responsif:** Melalui aturan @media (max-width: 767px), susunan halaman diadaptasi untuk layar perangkat seluler. Elemen di dalam header dan 

kartu proyek pada .card-list yang tadinya berjajar menyamping akan diubah menjadi tersusun dari atas ke bawah (flex-direction: column). 

