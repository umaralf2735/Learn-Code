# 04 - Fungsi di PHP (Function)

Sama seperti JavaScript, kita memanggil kekuatan pelimpahan tanggung jawab sub-pekerjaan dengan sebutan `function`.

## Sintaks Pembukaan

Mirip JS secara utuh:

```php
<?php
    function kasih_salam_pagi($nama_panggilan) {
        // Ttep pakai return klo mau hasil yang murni
        return "Salam Pagi Semangat, Bos $nama_panggilan!";
    }

    $pesan = kasih_salam_pagi("Jefri");
    echo $pesan;
?>
```

## Default Value (Penyelamat Ngekril)

Terkadang si Pemanggil bisa lupa mengirim paramater argumen. Untuk mencegah error PHP membunuh website kalian, beri dia *"Harga Default Darurat"* langsung dikurungnya dengan lambang = .

```php
<?php
    // Gak dikasih nama? Otomatislah isinya jadi "Pengunjung!"
    function tebakUmur($nama = "Pengunjung Anonim") {
        echo "Hai $nama. Tebakan umurnya gatau nih!";
    }

    tebakUmur(); // Output: Hai Pengunjung Anonim...
    echo "<br>";
    tebakUmur("Budi"); // Output Hai Budi....
?>
```
---
[⬅️ Sebelumnya: Array Assosiatif](../03-Array-Assosiatif/README.md) | [Lanjut ke Include Require ➡️](../05-Include-Require/README.md) | [🏠 Daftar Isi](../README.md)
