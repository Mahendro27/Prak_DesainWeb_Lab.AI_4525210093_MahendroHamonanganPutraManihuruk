# Nama:Mahendro Hamonangan Putra Manihuruk 

# NPM:4525210093 

MataKuliah:PRAK.DesainWeb 

# PERTEMUAN 7: 

|**No**|**Field**|**Input Uji**|**Hasil**|**Hasil Aktual**|
|---|---|---|---|---|
|**1**|Nama<br>Lengkap|"Al" (2 karakter)|Form menolak dan<br>menampilkan pesan error<br>_"Nama minimal harus 3_<br>_karakter."_|Pesan error<br>muncul di<br>bawah field<br>Nama Lengkap<br>dan pengiriman<br>form<br>dibatalkan.|
|**2**|Email|"mahendro.com"<br>(tanpa @)|Form menolak pengiriman<br>dan menampilkan pesan<br>_"Format email tidak valid_<br>_(contoh:_<br>_user@domain.com)."_|Pesan error<br>format email<br>muncul dan<br>data tidak<br>terkirim.|
|**3**|Nomor<br>Telepon|"0812abc345"<br>(mengandung huruf<br>/ < 10 digit)|Form menolak karena<br>tidak memenuhi regex ^[0-<br>9]{10,13}$ dan<br>menampilkan pesan error.|Pesan error<br>_"Nomor telepon_<br>_harus angka 10–_<br>_13 digit."_<br>muncul.|
|**4**|Alasan<br>Mengikuti<br>Event|"Ingin belajar" (13<br>karakter)|Form menolak karena<br>kurang dari batas minimal<br>20 karakter.|Pesan error<br>_"Alasan_<br>_mengikuti_<br>_minimal 20_<br>_karakter."_<br>muncul.|
|**5**|Upload<br>Identitas|File berkas<br>berukuran**3.5 MB**<br>(.exe atau .pdf<br>terlalu besar)|Form menolak berkas dan<br>menampilkan pesan<br>_"Ukuran file melebihi 2MB_<br>_atau ekstensi tidak_<br>_diizinkan!"_|Pengiriman<br>form dicegat<br>JavaScript dan<br>pesan<br>kesalahan file<br>muncul.|



