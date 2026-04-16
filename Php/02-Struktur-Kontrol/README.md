# 02 - Struktur Kontrol PHP

Logika pengatur alurnya sangat generik dan mirip dengan induk C-Family (C++, JS).

## 1. If / Else
Untuk mengecek boolean logika.

```php
<?php
    $duitKu = 50000;

    if ($duitKu >= 50000) {
        echo "Wow, uang banyak, beli pizza!";
    } elseif ($duitKu > 10000) {
        echo "Cukup beli mie rebus di warkop.";
    } else {
        echo "Aduh.. harus puasa dulu..";
    }
?>
```

## 2. Perulangan Logis

Sama kuatnya seperti biasa, pakai inisiasi standar `for`:

```php
<?php
    // BACA: Untuk i = 1; Muter selama i blm tembus 10; naikin i++  
    for ($i = 1; $i <= 5; $i++) {
        echo "Peserta Lomba Ke-" . $i . "<br>"; 
        // Note: di PHP, kita pake Tanda Titik "." untuk menyatukan String!! (Bukan tanda plus ahaha)
    }
?>
```

---
[⬅️ Sebelumnya: Dasar-Dasar](../01-Dasar-Dasar/README.md) | [Lanjut ke Array & Assosiatif ➡️](../03-Array-Assosiatif/README.md) | [🏠 Daftar Isi](../README.md)
