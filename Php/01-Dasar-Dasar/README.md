# 01 - Dasar-Dasar PHP

PHP itu ditakdirkan hidup menyusup di dalam HTML. Makanya untuk memberitahu Komputer kalau bagian ini itu area "Server", kamu harus menggunakan gerbang penutup ajaib `<?php ... ?>`.

Semua *statement* murni kamu **Wajib ditutup dengan titik koma** (;)!

## 1. Menulis Halaman (Echo)

Dulu sewaktu blm ada JS DOM, mengubah website di layar sangat sulit. Di PHP kalian mencetak HTML di layar memakai jurus `echo`.

```php
<html>
    <body>
        <h1>Halooo Tampilan Luar Biasa!</h1>
        
        <?php
            // INI ADALAH LOGIKA PHP PENGENDALI SERVERNYA
            echo "<p>Saya paragraf ajaib yang muncul karena PHP gaiss</p>";
        ?>
        
    </body>
</html>
```

## 2. Sang Penguasa Dolar `$` 

Berbeda dengan Javascript (`let`) yang repot. Apapun variabel di PHP kamu WAJIB menggunakan Lambang Uang alias Tanda Dolar (`$`) untuk menjabarkannya. Tanpa ini maka nilainya Error total.

```php
<?php
    $namaLengkap = "Udin Sudin"; // Otomatis String
    $umur = 17; // Otomatis Int

    // Mirip JS literal string. Kalau pakai kutip ganda ("..."), variabel langsung bisa di suntal ke dalem!
    echo "Pagi bang, perkenalkan saya $namaLengkap usia saya udah $umur taun.";
?>
```

---
[Lanjut ke Struktur Kontrol ➡️](../02-Struktur-Kontrol/README.md) | [🏠 Daftar Isi](../README.md)
