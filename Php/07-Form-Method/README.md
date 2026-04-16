# 07 - Menangkap HTML Form (Mencuri Lemparan Data POST & GET)

Di Frontend/HTML kalian biasa main ngisi Form Login Pendaftaran. Siapa yang nerima data email login dan password itu? Jawabannya variabel gaib PHP bernama `$_POST` atau `$_GET`.

## Bedanya GET dan POST

- **`$_GET`** :  Kalau diklik Submit, isian datanya bakal terpampang jelas ngeriuk di URL atas (contoh `web.com/?user=budi&umur=10`). GA AMAN BUAT PASS! Cocok buat Fitur *Search*.
- **`$_POST`**: Disembunyikan di dalam jeroan selimut internet (Request bodi tak terlihat). Aman Sentausa untuk Password!

## Eksekutor PHP yang Siap Nampung

**1. KITA PUNYA FILE FORM (`index.html`)**
```html
<form action="proses.php" method="POST">
    Nama Anak: <input type="text" name="namaCakep">
    <button type="submit">KIRIM!</button>
</form>
```

**2. KITA PUNYA TUKANG NADAH NYA (`proses.php`)**
```php
<?php
    // Kuncinya itu di atribut (name="...") HTML kalian tadi
    
    // Ngambil pakai kunci rahasianya!
    $namaTangkap = $_POST['namaCakep'];

    echo "<h1>Wah yang ngirim ternyata bos $namaTangkap!</h1>";
?>
```

Kalian sudah menyentuh 50% rahasia dari aplikasi pengolahan Fullstack web sedunia! Form adalah tulang punggung website dinamis.

---
[⬅️ Sebelumnya: OOP Dasar](../06-OOP-Dsr/README.md) | [Lanjut ke Session ➡️](../08-Session-Cookie/README.md) | [🏠 Daftar Isi](../README.md)
