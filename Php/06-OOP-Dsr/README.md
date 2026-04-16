# 06 - Pemrograman Objek (Class) PHP Modern

PHP sejak dirilis versi 5 (Sekitar belasan tahun lalu) berubah wujud merombak jeroannya dan mewajibkan semua programmernya beralih berkiblat pada OOP mutlak.

Kalian tidak mungkin bisa memahami betapa menabjubkannya memanggil database di Framework **Laravel atau CodeIgniter** apabila tidak tau dasar perakitan Class di PHP. Semua framework web PHP merancang *Router*, *Controller*, hingga *Model Database* MURNI MENGGUNAKAN CLASS Blueprint!

## 1. Blueprint PHP (Memahat Kelas)

Sama kek Java murni, strukturnya memakai kurung kurawal. Parameter pemanggilan anak didalamnya menggunakan *Variabel Sakti Pengganti Nama*:  `$this` diikuti dengan panah setrip (`->`).

```php
<?php

class KucingGarong {
    // PUBLIC = Boleh dibuka paksa/dicolong data isian ini dari program luar setelah dia lahir jd kucing jadi Jadian!
    public $nama_hewan;
    public $suara_hewan;
    
    // PRIVATE = Kesehatannya cuman dia yg bs baca. Dokter lwar kaga bs tau. (Security Enkapsulasi)
    private $umurBulannya;

    // CONSTRUCTOR : Si 'Method Pembuka Gerbang' Yg akan otomatis hidup Pertama Kali ketika kucing dicipakan k bumi! (Pake pnjaga Double underscore `__`)
    public function __construct($nama, $suara, $bulan_umur) {
        
        // Ngisi organ tubuh yang kosong tadi dgn paramatr masukan alam! (Gunanakan panah ya bos bukan TITIK kl di PHP)
        $this->nama_hewan = $nama;
        $this->suara_hewan = $suara;
        $this->umurBulannya = $bulan_umur; 
        // 👆 Aman krna ini masih di dlm perut class nya sndri jd bisa di edit wlupun private!!
    }

    // Method Tindakan
    public function bernyanyiGila() {
        echo "Si Aneh $this->nama_hewan lagi teriak woi!! Bilang: $this->suara_hewan !!! <br>";
    }
}

// ------ DILUAR SANA WAKTUNYA KITA PAKE CETAKAN KUE INI -----

// Bikin Kucing Realitanys Pakai kata maut NEW
$kucingSiam = new KucingGarong("Si Manis Belang", "Meoonnnggg Panjangg!!", 5);

// Manggil Aksinya (DI PHP BUKAN PAKE DOT / TITIK KAYA JS YA! TAPI PAKAI PANAH -> )
$kucingSiam->bernyanyiGila();

// Nembak langsung ngganti nama (Krn Public)
$kucingSiam->nama_hewan = "Ujank Hitam";
// $kucingSiam->umurBulannya = 100; // ❌ ERROR FATAL DITOLAK!! UMUR BULANNYA PRIVATE! GABOLEH DITEBUK DARI LUAR DONG!

?>
```

Gaya Pembagian file Objek Class  inilah (berserta konsep *Namespace* pengikat import turunannya) yang menjadi darah utama ekosistem kodingan Framework Website sedunia! Seluruh logika kalian nyatet/ngapus postingan blog.. akan dibungkus rapi dalam perut Class `ArticleController`! Luar biasa bersih..

---
[⬅️ Sebelumnya: Nge Belah Puzzel File HTML](../05-Include-Require/README.md) | [Lanjut ke Nyedot Formulir HTML ➡️](../07-Form-Method/README.md) | [🏠 Daftar Isi](../README.md)
