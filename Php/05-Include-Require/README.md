# 05 - Include & Require (Sihir Lego Membelah File)

Kalian pasti pusing kalau nyari file di `index.php` yang kodenya sampai 2,500 baris campur aduk isinya Logic DB, Footer Copyrtighyt Html, Sidebar CSS Menu Kiri, Menu Atas Navabr HTML dll?! Scrollnya aja udah bikin mati jari.

Pecah Dong!!! File Navigasi Atas taruh di file terpisah. CSS Sidebar pisah beda kamar!! Trus gmn biar mreka nyambung jadi 1 layar Web utuh di mata User internet sana?? PHP jagonya jahitan komponen!

## Aturan Jahitan: `include` vs `require`

Keduanya sama sama berfungsi "Narrik jaroan file seblah dan dicopasin plek ketiplek kesini" Tapi sifat galaknya berbeda :

### 1. `include` (Sifatnya Kendor Copasnya)
Kalau file yang mau disedot ternyata HILANG / LUPA DISAVE / NAMA TYPO.. PHP bakal teriak merah *[Warning]*. TAPI program halaman web kalian **MASIH HIDUP LANJUT JALAN NGE RENDER SAMPE KE FOOTER BAWAHNYA!!**

Sangat aman baut dipake naro Header atau Widget cuaca ga pnting yang hilang gpp.

```php
// File PUSAT: index.php !!!!
<html>
<body>

<?php
// NYEDOT POTONGAN HTML DARI FILE SABLH!! (navbar atas item menu Home/About)
include("menu_navbar_atas.php");

// Kalo ternyata nama_file ini gw typoin/ilang.. Dia ngeluarin wARNING tp brs d bwh msi kepnnngil.
?>

<!-- SISA KONTEN BADAN WEB -->
<h1>Isian Berita Utama Harian Koruptor Ditangkap....</h1>

</body>
</html>
```

### 2. `require` (Sifat Mutlak Kematian Mati Blank)
Dilarang ngeles! Kalau si file incaran dihapus orang. Maka Layarmu **FATAL ERROR DAN PUTIH BLANK MATEEE SEGALA SISANYA GA JALAN!**. Tidak ada kata maaf.

Berarti INI SANGAT WAJIB DIPAKAI UNTUK: Menyedot Logika PHP Database!! (Yakali Databsenya Typo Ilang, terus Web nya mau jalan pake data hantu darimana?? wkwk mending matein paksa!).

```php

// FILE UTAMA LUAR
<?php
    require("inti_rahasi_core/koneksi_database.php"); 
    // ^-- Klo error, baris bawah gabakal diproses lgi dijamin gbs msk
    
    echo "Lanjut menarik data SQL dr tbel user....";

    // Jaman modern pada pake imbuhan '_once' lbih bgus lg!
    require_once("tools_hitung_pajak.php") 
    // ^-- Sama aja tpi dia ngecek: Kalo udh ketarik ga ush ditarik copyan smpe double di memory ya klo gue lp mangggi lg.
?>
```

Kalian anak Frontend atau Fullstack yang sering bkin tema WordPress / Toko Baju onlie, Ilmu Include membelah belah Partikel ini sangat membatu rapi nya Struktur Folder File Web yang berlembar-lembar tsb (Moduler!).

---
[⬅️ Sebelumnya: Fungsi](../04-Fungsi/README.md) | [Lanjut ke OOP Cetakan Framework Bintang ➡️](../06-OOP-Dsr/README.md) | [🏠 Daftar Isi](../README.md)
