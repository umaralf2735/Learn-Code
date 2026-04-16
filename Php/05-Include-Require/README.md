# 05 - Menyatukan Potongan File (Include & Require)

Tidak mungkin kamu membuat Website Toko Online yang Header-nya, Sidebar-nya, Footer-nya dan isi kontentnya dicampur dalam 1 file `index.php` sampai 10 ribu baris.

PHP punya kemampuan instan menarik isi file PHP lain buat dijahit ke layarnya secara sakti!

## `include` vs `require`

Kedua komando ini gunanya kembar, bedanya cuma di "Sifat Mengamuk-nya PHP".

### `include` (Boleh Copas)
Kalau filenya gak nemu (gak ada), dia cuman ngeluarin peringatan (*Warning*), tapi kode dibawahnya **TETEUP DIJALANKAN LANJUT TERUS**.

```php
<!-- ISI DARI FILE (atas.php) -->
<html>
<head><title>Websiteku</title></head>
<body>
    <h1>NAVIGASI ATAS</h1>
```

```php
<!-- ISI DARI FILE (index.php) -->
<?php
    // MENYEDOT ATAS PHP!!
    include("atas.php"); 
?>

<!-- SISA KONTEN BAWAHNYA -->
<p>Selamat datang di Website Udin..</p>
</body>
</html>
```

### `require` (Syarat Mutlak Keras)
Dilarang ngeles! Kalau si file `fungsi_berat.php` nya dihapus orang/hilang. Maka Layarmu **FATAL ERROR DAN PUTIH BLANK**. Tidak memaafkan.

Ini sangat cocok dipakai buat menaruh file konektor rahasia Database! Ya kali database ga nyangkut program jalan terus!

```php
<?php
    require("koneksi_database.php"); 
    // ^-- Klo error, baris bawah gabakal diproses.
    
    echo "Lanjut menarik data SQL...";
?>
```

---
[⬅️ Sebelumnya: Fungsi](../04-Fungsi/README.md) | [Lanjut ke OOP PHP ➡️](../06-OOP-Dsr/README.md) | [🏠 Daftar Isi](../README.md)
