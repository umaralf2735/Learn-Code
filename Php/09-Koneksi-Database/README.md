# 09 - Menarik Darah Database MySQL (Ilmu Sihir Hitam PDO)

Kita uda pegang List Array dari List Form anak-anak pendaftar OSIS. Tapi sedih, Begitu Komputernya (XAMPP Servernya) PC nya dimatikan aliran Listrik nya (Shut Down Laptopnya).... 

**Boooooooooooooooooom! Semua Variable Data di Memori RAM Hilang tdiak berbekas Jadi NOL !!**

Satu-satuntay cara membuat data mu abadi dan abisa dibaca Jutaan orang luar adalah kamu Harus menyimpan / ngoper nya secara Realtime masuk kecelorot Database `MySQL` / Postgresql aslimu!

PHP dari leluhurnya punya jembatan kuno yg hancur lebur namany (mysql_query / mysqli). **JANGAN PAKE ITU! KAMU BISA DIHACK MULLYARAN UANG LEWAT SQL INJECTION!!**

Masuki Jembatan Canggih Anti-Tembus: **PDO (*PHP Data Objects*)**.

## Buka Gerbang Bawah Tanah (Konektor Db) Menggunakan Keamanan `Try..Catch` !

Biasanya dlu kita ngetik ini dipartisi file namanya `koneksi.php` aja. Trs nanti di Include / Require 1 file ini kemana mana halman webnya.

```php
<?php
// ALAMAT Servernya!! (Kl XAMPP Lokal PC Lu, brrrti Namanya 127.0.01 / Locahost!)
$host = "127.0.0.1";
// NAMA DATABASE YG UDAH LU KREAT D DALEM MYSQL NYA sblunmya!!
$namaDBSakti   = "pabrik_tahuku"; 
$userKetik = "root"; // Default XAMPP Windows ganti2 gpp
$passDB = "";        // Klo xampp default kosongan ya bskr

// KRN INI MENGHUBUNGI MESIN LAIN DI LUAR SANA, RENTAN PUTUS KONEKSI!! PASTIKAN PAKE TRY CATCH TAMENG PENANGKAP BOM :
try {
    
    // Menyusun jimat mantra String PDO nya bwt buka gerbang
    // INILAH BARIS YG NGEBONGKAR DAN NYALURIN PIPA NYA:
    $pdoGerbangKoneksi = new PDO("mysql:host=$host;dbname=$namaDBSakti", $userKetik, $passDB);
    
    // Oh iya, PDO by default mode diam ga mrh klo salah kodingn.. Paksa dia klo lu slah njalanin script dia bakal Ngluarin Errro ke CATCH!!
    $pdoGerbangKoneksi->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);
    
    // >>>>> DISINILAH SEBENERNAYA TARIKAN KODE MURNI MYSQL BERAKSIII <<<<<<<<
    $pertanyaanSQLQyery = "SELECT * FROM daftar_karyawan_tangguh LIMIT 5";
    // Mnuterin kuncinya!
    $stmObjekMesinCetak = $pdoGerbangKoneksi->query($pertanyaanSQLQyery);
    
    // HASIL CETAKNNYA MANTAP JIWAAAA!!!!! DIA NGEBUANG SEDOTAN ITU JDI ARRAY ASSOSIATIF PHP MURNI BENERAN!!!!
    $semuaBarisanPekerja = $stmObjekMesinCetak->fetchAll(PDO::FETCH_ASSOC);
    
    // Buka datanya ke html pke Loop Biasaa Array foreachhh ahahah!!
    foreach($semuaBarisanPekerja as $barisOrang) {
        // (nama_dihartanya) ADALAH NAMA KOLOM DI DB TABEL MYSQL LUU !
        echo "Nama Yth: " . $barisOrang['nama_dihartanya'] . " Dia Gajinya Rp " . $barisOrang['bayaran_gaji'] . "<br>";
    }

} catch (PDOException $e) {
    // Kalau salah Password Root Db lu.. Mesin XAMPP mu gk bakal Error Putih Hancur.. Dia melompoaptt kesini memuntahkan Pesnananya!!
     echo "Adudduhhh Kiamat Tembok Database Runtuh Bangt: " . $e->getMessage();
}
?>
```

KITA TIDAK MUNGKIN MENGETIKAN "INSERT USER BARU" tanpa Bind Param (Sihir pengaman PDo anti SQL Injecton form hacker). Nmuun pada intinya, kamu kini sdhl melihat Mukzizat perpaduan Database Menjadi Array, dan Array PHP di Foreach mnajadi Tag Html di Browsernya Client. Selamat!! Fullstack Engineering Fundamental u Tuntas!

---
[⬅️ Sebelumnya: Gembok Memorui Server](../08-Session-Cookie/README.md) | [Lanjut ke Alat Pihak Ketiga Dewa ➡️](../10-Composer/README.md) | [🏠 Daftar Isi](../README.md)
