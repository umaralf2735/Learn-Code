# 04 - Fungsi di PHP (Membuat Tukang Mandiri)

Gak asik lah ngetik hitung Pajak PPN 11% copas sampe 300 baris. 

Kita bungkus logika penghitungannya dalm sebuah `function`. Kunci mutlak di PHP sama seperti JS murni. Dia bisa dikembalikan hasilnya (*return*), tapi sayangnya PHP kolot tidak terlalu ramah dengan Arrow Function `=>` gahoel punyanya JS wkwkwk.

## 1. Syntax Pembukaan Pekerja

```php
<?php
    // Deklaraiin nmanya!
    function alatBikinKopi($jenisBubuk) {
        $mesinMuter = "Brrrrr... Kopi " . $jenisBubuk . " Sedang disaring...";
        
        // RETURN ITU WAJIB BUAT MO TAMPILIN BALIK DATA! Klo cuman print di dalem ini si fungsi g guna didlm proses luar db (Void).
        return $mesinMuter;
    }

    // Manggil fungsinya pake kurung ( ) ! Masukin data prmnya!! (Argument dipas ke parameter)
    $gelasPelanggan = alatBikinKopi("Kapal Api Murni");
    
    echo $gelasPelanggan;
?>
```

## 2. Penyakit Scope Bawaan PHP (`global`) Cacat Bawaan!
**BAHAYA PEMULA!!!**

Berdeda dengan Python / Golang / JS: Kalau kamu bikin Toren tangki Air (Variabel) ditaruh diatas Fungsi di luar, terus fungsi dibawahnya pingin ngintippp / narik srotan dari air tersebut. DI BAHASA LAIN BISA!! 

**TAPI DI PHP, FUNGSI ITU KEDAP SUARA TERTUTUP ISOLASI TOTAL!!! GABISA BACA VAR LUAR!!!** 

```php
<?php
$gajiKantor = 100;

function tambahGajiPalsu() {
    // ❌ ERROR "UNDEFINED VAR $gajiKantor !!!" (KITA GA KENAL DI DALEM PENJARA GAK ADA KONEKSI).
    $gajiKantor = $gajiKantor + 50; 
}
?>
```

**SOLUSINYA (Jebol Dinding Penjaranya Pakai `global`):**

```php
function tambahGajiBeneran() {
    global $gajiKantor;  // MANTRA PENJEBOL ISOLASI!!!
    $gajiKantor = $gajiKantor + 50;  // BARU BERHALSI DITMBAHA!
}

// Tapi para programmer php Dewa bilang : JANGAN SERING PAKE GLOBAL. Bahaya gampang kena hack timpa variabel silang!
// Mending Pake Jalan Depan yang Legal: lewat argumen Parameter Funcitonnya bos!!
```

## 3. Harga Nilai Backup Darurat (Default Value)

Website ngecrash Blank White kalau kalian nyuruh si `alatBikinKopi()` tapi lupa ngirimin `$jenisBubuk`?!

```php
<?php
    // Gak dikasih bubuk? Otomatis pasangin Kopi Ireng murahn..
    function sisaSumbanganGerebek($danaMasuk = 0) {
        echo "Lhooo daper rejeki nomplok senilai: $danaMasuk juta bos.";
    }

    sisaSumbanganGerebek(); // Output: daper sumbangan... 0  ... (GAK ERROR! AMAN! PHP DISELAMTAKAN DR CRASH LAYAR BLANK).
    echo "<br>"; // spasi Html
    sisaSumbanganGerebek(999); // Output ... dapt 999 
?>
```
---
[⬅️ Sebelumnya: Kamus Array Data](../03-Array-Assosiatif/README.md) | [Lanjut ke Memecah File Website (Lego) ➡️](../05-Include-Require/README.md) | [🏠 Daftar Isi](../README.md)
