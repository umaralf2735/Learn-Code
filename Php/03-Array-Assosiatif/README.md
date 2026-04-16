# 03 - Menggali Harta Karun Array & Array Assosiatif

Kalian kalau ngoding Javascript punya Array Cuman buat naruh list `[Udin,Budi]`. Klo list ny pnting ber identitas nnti Javascript harus repot bngun `Object {} JSON -> {nama: udin, levl: 50}`. Beda wujud!!

Di PHP.. **SEMUANYA ADALAH ARRAY!** Mau list laci besis, ataaupun yg berupa Dictionary Label JSON... Seluruhnya adalah Array super ghaib. Karena di PHP data asalmnya dari Datbase (Yg dmana itu tabel MySQL kan).

## 1. Array Kosongan Primitive (Indeks Nomor `[]`)

```php
<?php
    // Bikin array baru  Prtama pake siku biasa
    $tasSenjata = ["Panci", "Pisau Lipat", "Ketapel"];

    // Kalo lu pake Javascript mau nambah barang hrs pake .push()
    // KALO DI PHP: Ketik aja siku kosong murni di blakng nmanya lgsg di isi ke tmpat kosong brkttnya wkwk (Aneh bin Ajaib kn!)
    $tasSenjata[] = "Batu Krikil";

    echo "Senjata peratama sy aalah njrr : " . $tasSenjata[0]; // Output: Panci
?>
```

## 2. Array Bersimbol Muka Kunci (ASSOSIATIF Array)

Ini adalah ujung tombak kalian! Javascript nyebut ini JSObject `{ }`. PHP cukup bikin Array Biasa trus nimpain `=>` sebagai Kunci Gembok ke Data Valuenya.

```php
<?php
    // Kiri = Kuncinya, Kanan = isinya
    $profilGuruPNS = [
        "namaHli"    => "Pak Raden Sudirja",
        "jabatan"    => "Kepala Sekolah",
        "tunjangan"  => 5500000,
        "is_pensiun" => false
    ];

    // Ngambilnya? Gausah . , tapi pakailah Kuncinya masukin dlmKurung Siku!!!
    echo "Gaji bos bulan ini sisa: " . $profilGuruPNS["tunjangan"];
?>
```

## 3. Trik Meloop Foreach Sangat Sakti

Kamu ngereturn array dri databse isinya ratusan objek user bgituan td, mo di tempel nampilin di Layar kan pake tabel satu2?
`foreach( arrayNYAAA as PENGANTONGINYA => BARANGNYA )` 

```php
<?php
    $nilaiRapor = [
        "BudiKocak" => 55,
        "SusiRajin" => 90,
        "JoniMamet" => 60
    ];

    // Putarr mesin bang!!! (Tangkp dlm variable string &kembalinnya gbebss)
    foreach ($nilaiRapor as $nickPeserta => $poinNilai) {
        // Didalam loping sini.. Si nick dan Poin itu ganti ganti identitas sbnyk 3 kli!
        echo "Nilai Mahasiwa sngatt luar biaasa : $nickPeserta -> Memiliki Score Final $poinNilai !! <br>";
    }
?>
```

Dengan menguasai dua sistem ini, framework apapun entah CodeIgniter atao Laravel yg ngereturn Objek Eloquent. Inti saringannya adalah cuman berpusan puteng Array Assosisatfif di looping `Foreach` sperti td lalu ditempeklkan tag `<html div>` didalam echonya! Boom jd dah aplikasi web dinamis!!

---
[⬅️ Sebelumnya: Struktur Kontrol Loop](../02-Struktur-Kontrol/README.md) | [Lanjut ke Fungsi Mandiri ➡️](../04-Fungsi/README.md) | [🏠 Daftar Isi](../README.md)
