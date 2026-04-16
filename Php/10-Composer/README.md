# 10 - Belanja Senjata di Composer

Tahap puncak dari master PHP. Sama halnya seperti JS punya NPM (Node Package Manager). PHP Punya yang selevel sakralnya. Yaitu **Composer / Packagist**.

Composer bukan bagian bawaan PHP, ini adalah program ajaib buatan komunitas yang harus didownload manual sekali, yang merubah cara programmer PHP dunia bekerja menyusun *Framework* hingga akhir zaman. (Contoh Framework idola : Laravel / Symfony).

## Menarik Keajaiban Modul Luar 

Buka terminal CMD mu (Pastikan php path nyantol & composer dah diinstall):

```bash
composer init
```
Kemudian unduh library luar super kompleks (misal untuk bikin fitur Email / PDF Otomatis), kita coba alat manipulasi Waktu tingkat dewa `Carbon` punyanya Laravel.

```bash
composer require nesbot/carbon
```

Seketika sebuah Folder super berat `vendor/` dan `composer.json` numpang ke dalam direktorimu!

## Cara Menyalakan Mesin Pihak Ketiganya di Kodingan

Hal terkeren adalah. Sesudah file kita berantakan ketambahan library luar, kita CUKUP MENARIK KABEL UTAMA SAKLARNYA! (Autoloader).

```php
<?php
// Trik ini menarik ratusan ribu library luar hanya dgn 1 kode sebaris!!!
require 'vendor/autoload.php';

use Carbon\Carbon; // Kita pasang nama kelas nya yg kita pengen

// BOOM! Tiba tiba kita punya kecerdasan manipulasi waktu di detik ini jg
echo "Sekarang jam: " . Carbon::now()->toDateTimeString() . "<br>";
echo "Minggu depan itu tanggal berapa sih? " . Carbon::now()->addWeek()->toDateString();
?>
```

*Welcome to Real World of Advanced Software Engineering.* Selamat, kamu sekarang sah masuk jembatan *Mid-Level* Engineer!

---
[⬅️ Sebelumnya: PDO Database MySQL](../09-Koneksi-Database/README.md) | [🏠 Daftar Isi Utama](../README.md)
