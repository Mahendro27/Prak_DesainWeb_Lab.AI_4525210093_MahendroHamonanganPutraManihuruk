Nama:Mahendro Hamonangan Putra Manihuruk 

NPM:4525210093 

MataKuliah:PRAK.DesainWeb 

PERTEMUAN 5: 

# **Struktur HTML (index.html)** 

- **Header & Navigasi** : Bagian atas halaman berisi elemen <header> yang memuat logo dan judul toko. Di bawahnya terdapat elemen <nav> berisi tautan menu utama seperti Beranda, Kategori, Produk, Keranjang, dan Kontak. 

- **Layout Utama (<main>)** : Dibagi menjadi dua bagian utama menggunakan elemen <aside> sebagai _sidebar_ di sebelah kiri untuk daftar kategori produk, dan <section> di sebelah kanan sebagai area konten utama. 

- **Area Konten** : Terdiri dari elemen .hero (banner ucapan selamat datang beserta tombol aksi) dan .card-container. .card-container menampilkan tiga kartu produk (Kemeja Flanel, Sepatu Sneakers, Jam Tangan), yang masing-masing dilengkapi gambar _placeholder_ , nama produk, harga, deskripsi singkat, dan tombol "Tambah ke Keranjang" yang memanggil fungsi JavaScript tambahKeKeranjang(). 

- **Footer** : Bagian bawah halaman memuat informasi hak cipta dan kontak. 

# **Desain & Styling CSS (style.css)** 

- **Penggunaan Flexbox** : CSS ini sangat bergantung pada properti Flexbox (display: flex) untuk mengatur tata letak komponen. Flexbox digunakan pada .header, .navbar, .layout (untuk menyandingkan sidebar dan konten), serta .cardcontainer (untuk menyejajarkan kartu produk). 

- **Tema Visual Wireframe** : Desainnya menggunakan palet warna abu-abu (monokrom) dengan batas garis tegas (solid dan putus-putus/dashed). Hal ini memberikan tampilan yang rapi dan menyerupai _wireframe_ atau _mockup_ . 

- **Desain Kartu Produk (Card)** : Elemen .card dirancang dengan flex: 1 dan flexdirection: column agar ukurannya seragam. Deskripsi produk (p) menggunakan flex-grow: 1, yang berfungsi untuk mendorong tombol "Tambah ke Keranjang" agar selalu sejajar di bagian paling bawah kartu. 

- **Desain Responsif (Mobile-Friendly)** : Terdapat _Media Query_ (@media (maxwidth: 768px)) yang secara otomatis mengubah struktur halaman pada layar kecil (seperti ponsel). Pada mode ini, _sidebar_ dan area konten yang tadinya bersebelahan akan disusun menjadi atas-bawah (flex-direction: column), begitu pula dengan kartu-kartu produk. 

- **Animasi Toast Notification** : Terdapat gaya CSS tersembunyi untuk elemen #toast yang dirancang sebagai pop-up notifikasi (pengganti _alert_ standar) dengan animasi _fade-in_ dan _fade-out_ , meskipun elemen HTML-nya belum dituliskan di dalam berkas index.html. 

