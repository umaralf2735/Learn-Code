# 07 - Menangkap Jebakan HTML Form (Mencuri Lemparan Data POST & GET)

Di Frontend UI/UX design (HTML/CSS) kalian susah-susah main warna ngasih kotak isian Form Pendaftaran dan Tombol *"Daftar Login"*. Trus... pas usernya nge-ngetik password lu mencet tombold daftar, SIAPA DI SERVER YANG BAKAL NAMPUNG CATETAN NAMA dan PASWORD TADI KE DATABASE?!

Yak! Jawabannya variabel array gaib milik dewa PHP bernama array superglobal `$_POST` atau `$_GET`.

## Sifat Menipu GET dan Keamanan Baja POST

Halaman Form dan Halaman Tujuan Proses Server adalah 2 entitas beda. Gimana cara formulirnya terbang menyberangi lautan internet??
* **`$_GET`** :  Kalau diklik Submit, mesin browser bakal mengikattulisan isian datanya dipaparkan panjang banget Telanjang Bule gda sensor  **di Kolom URL Browsermu yg atas itu** *(contoh Webnya brubah jd kek gini diblaknbyA: `web.com/login.php?usermku=budi&passTae=10xca`). GA AMAN BUAT PASS! Cocok buat Fitur *Search*.
* **`$_POST`**: Menyimpan dan Membawanya ngumpet menyusup ke bawah tanah dlm Payload Http tanpa merusak kebersihan URL Bar atas kamu!! Password 100% AMAN! Rute Default para Programmer handal web.

## Demo Eksekutor Pencidukan Data isian:

**1. KITA PUNYA HTML HALAMAN AWAL PENGISIAN FORM (`halaman_daftar.html`)**
```html
<!-- KITA LEMPAR PAKE ALAT METHOD KUDAC POST NGERAH TABRAK KE FILE SEBELA PROSES!! -->
<form action="proses_tangkap.php" method="POST">

    <!-- "name" ADLAH LABEL KUNCI ARRAY MU NANTI DI PHP NYA!! -->
    Username: <input type="text" name="namaKerenAksi">
    
    Password: <input type="password" name="sandiBokep">
    
    <button type="submit">GAS DAFTAR OM!</button>
</form>
```

**2. FILE GUDANG SERVER DISBLH YG NYAMBUT TAMUNYA (`proses_tangkap.php`)**
```php
<?php
    // Gak Usah KAGET!!
    // Array $_POST SUDAH MATENG DIBWAIN KITA SAMA MESIN PHP SERVERNYA TINGGLAM COMOT!!
    // Pake kunci 'name' yang lu ketik di HTML mu sblmnya:
    
    $usernameUser = $_POST['namaKerenAksi'];
    $pwUser = $_POST['sandiBokep'];

    // Nah.. Biasanya disini data divalidasi dan di lempar ke INSERT MySQL di Database ...
    
    echo "<h1>Wih Makasih bos!! Atas nama: $usernameUser!</h1>";
?>
```

Gila ga tuh?! Kalian udah pegang 50% rahasia dari aplikasi Jual Beli Fullstack termahal di Dunia kek Amazon ato Shopee! Semua pesanan pembeli dihantar pake gerbong Form HTML ini dan ditangkap jala `$_POST` di server PHP Backendnya! Sempurna.

---
[⬅️ Sebelumnya: Class Objek Bungkusan](../06-OOP-Dsr/README.md) | [Lanjut ke Nyawa RAM Akun (Session) ➡️](../08-Session-Cookie/README.md) | [🏠 Daftar Isi](../README.md)
