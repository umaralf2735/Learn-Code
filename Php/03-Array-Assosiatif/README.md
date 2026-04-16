# 03 - Array dan Array Assosiatif

PHP sangat terkenal karena jago membaca data hasil query Database yang menumpuk. Maka ia membekali diri dengan sistem Dictionary tingkat dewa yang bernama **Assosiative Array**.

## 1. Array Kosongan (Indeks Standar)

```php
<?php
    // Bikin array baru (Bisa campur campur juga!)
    $laci_makanan = ["Odading", "Pukis", "Risol"];

    // Ngasih makanan baru nambah dibelakang dengan bracket kosong
    $laci_makanan[] = "Bubur";

    echo $laci_makanan[0]; // Output: Odading
?>
```

## 2. Array Bersimbol Muka Kunci (Assosiative)

Ini adalah wujud saktinya! Di Javascript dipanggil JSON Object. Di PHP, mereka ini cuman Array tapi pakai sistem Panah gemuk ( `=>` ).

```php
<?php
    $profilGuru = [
        "nama" => "Pak Raden",
        "jabatan" => "Kepala Sekolah",
        "kejam" => false
    ];

    // Ngambilnya? Pakai nama kuncinya di Kurung Siku!!!
    echo "Halo Yth: " . $profilGuru["nama"];
?>
```

## 3. Meloop Pakai *Foreach* (Sangat Canggih!)

Di Ruby kita kenal `.each`. Disini untuk muterin Map Assosiative-nya gunakan `foreach( ... as ...=>... )`.

```php
<?php
    $perolehanSkor = [
        "Andi" => 90,
        "Susi" => 80,
        "Joni" => 60
    ];

    foreach ($perolehanSkor as $namaUnik => $angkanya) {
        echo "Siswa $namaUnik berhasil mendapatkan poin sebesar $angkanya! <br>";
    }
?>
```

Kalian anak backend Database akan 1 Juta Persen menggunakan fitur di bab ini tanpa henti!

---
[⬅️ Sebelumnya: Struktur Kontrol](../02-Struktur-Kontrol/README.md) | [Lanjut ke Fungsi ➡️](../04-Fungsi/README.md) | [🏠 Daftar Isi](../README.md)
