# 06 - Pemrograman Objek (Class) PHP Modern

PHP sejak versi 5 berubah drastis menjadi kiblat OOP yang keras. Kalian tidak mungkin bisa memahami Framework Laravel atau CodeIgniter apabial tidak tau dasar Class di PHP.

## Blueprint PHP

Memakai kurung kurawal. Mirip struktur kelas Java. Parameter instan pemanggilan menggunakan panah setrip (`->`).

```php
<?php

class Kucing {
    // Public berarti bisa dibuka paksa dari luar setelah di copy
    public $nama_hewan;
    public $suara_hewan;

    // Constructor otomatis dipanggil lho (Pake double underscore)
    public function __construct($nama, $suara) {
        $this->nama_hewan = $nama;
        $this->suara_hewan = $suara;
    }

    public function bernyanyi() {
        echo "Si $this->nama_hewan lagi teriak $this->suara_hewan !!!";
    }
}

// Bikin Cetakannya Pakai kata maut NEW
$kucingBule = new Kucing("Belang", "Meeeong!!");

// Manggil Aksinya (Bukan Pake Titik, TAPI PAKAI PANAH -> )
$kucingBule->bernyanyi();

?>
```

Gaya OOP nilah (berserta konsep *Namespace* turunannya) yang menjadi darah utama ekosistem kodingan Web sedunia!

---
[⬅️ Sebelumnya: Include Require](../05-Include-Require/README.md) | [Lanjut ke Penanganan Bodi From ➡️](../07-Form-Method/README.md) | [🏠 Daftar Isi](../README.md)
