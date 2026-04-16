# 10 - Memanggil Senjata Alam Semesta (Composer Murni)

Javascript pnya Node Modules yang menuhin Hardishd (NPM). Bapak tua PHP ga mau kalah! PHP pamer **Composer / Packagist** yg luar biasa lebih efisien meracik dependency nyampai jutaan folder.

Dengan ini. Lu gabakal pusing kepanasan lg mikir "Gimana ya crnya aku bkin Fitue Cetak Invoice PDF dri Web PHP ini??". GA USAH BIKIN JEROAN NYA! Copas aja pustaka (Library) yang udh dibikin sama jutaan profesor d github dr belahan dunia sanah make sihir Composer Package Mananger (NPMnya dunia PHP!!). Framework gila idaman indonesia macam *Laravel / CI4 / Symfony* Semuanya diracik dan dihidupkan lewat mesin ini doang.

## 1. Menarik Keajaiban Modul Luar 

Sama sperti npm atau pip python. Buka Terminal CMD mu (Kalau composer udh lu install global di windows lo):

```bash
# Inisiasi Bikin Buku Proyke (composer.json)
composer init
```
Kemudian unduh library luar. Misal di prusahaan startup elo dituntut bsa **Manipulasi Tanggal +3 Hari dr bsok Hari Rebu pake Bhsa indonesia blbalaala** (klo php polosan kan pusing bgt itu logic angkanya brp hr, dll detek2ny). Manggil pustka Dewa manipulaWkatu namaya *Carbon* (Ini alat mautnya pnya lAravel lho).

```bash
composer require nesbot/carbon
```

Seketika sebuah Folder super berat `vendor/` dan `composer.json` numpang menetes dan beranank meneteas ke dalam direktori file PHP mu itu!

## 2. Cara Menyalakan Listrik Mesin Pihak Ketiganya Secara Auto di Kodingan App Lu! (Keasikan AutoLoad)!!!

Inilah keunggulan kawan lama dibnding JS ES 6 yg repoot Import Export satu satu ke titik lokasi slash Folder librarynya (pusinggg nyarinua). PHP menggunakan **Autoloader Ajaib!**.

Lo cumn PERLU MANGGIL 1 NAMA FILE VENDOR AUTOLOAd DI PALING ATAS PUSAT ROOT FILE `.php` MU DOANK !! Sisanya.. Jutaan libraliy dibawahnya akang kesedot nempel di class memory tanoa perlu di include lagi kmn mnaa!!

```php
<?php
// TRIK DEWA MENARIK RATUSAN RIBU LIBRARY LUAR HANYA DGN 1 KODE SEBARIS INI!!
require 'vendor/autoload.php';

// NAh kalau udah gito... Lu bebas comot manggil NAMA CLASS Class aneh yg lu donlot dimanapun!
// Tarik klsnya:
use Carbon\Carbon; 

// BOOM! Tiba tiba kita punya kkuatan magic dr mesin Carbon murni!!
echo "Hallow bos, Sekarang jam: " . Carbon::now()->toDateTimeString() . "<br>";

echo "Oh ya gann, Minggu depan itu di tanggal dan hari apa yah? Ini Jwbanya: " . Carbon::now()->addWeek()->isoFormat('dddd, D MMMM YYYY');
?>
```

Bayangkaan kalau elo pake Date bawaan PHP Murni, bkal puluahn baris lu mecah Array Bulan trs digantu transalte jd teks...
Pake Carbon CUMN Butuh Nnambah Fungsi `.IsoFOrmat(dddd, dll)` nyaaa!! wkwkwk!!

*Welcome to Real World of Advanced Web Fullstsck Software Engineering.* 
Lu udh tamat baca 10 Modul PHP Terkuat sejagat ini?  **Selamat!!, Pergilah mendonwload Composer, tarik *Laravel Versi 11*.. dan melangkah merajut 10-20 Juta / Bulan dari karir Freelancer maupun Perusahaan korporat raksas Jakarta!!**

---
[⬅️ Sebelumnya: Magic PDO Array Database](../09-Koneksi-Database/README.md) | [🏠 KEMBALI KE DAFTAR ISI UTAMA PHP MURNI](../README.md)
