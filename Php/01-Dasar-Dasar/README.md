# 01 - Dasar-Dasar PHP (Membangkitkan Roh HTML)

PHP: Diciptakan saat Dinosaurus Web masih hidup (Tahun 1995-an). Tapi coba tebak siapa yang masih jadi penguasa tunggal menopang berdirinya 70% Blog, Toko Online, Web Berita (WordPress), sampei forum dunia hari ini? Yes. PHP.

## Filosofi "Penyusup yang Baik"

Kalau Javascript ngerun di PC-nya Pemain/User (Maka disebut *Frontend Browser*). PHP itu hidup di Alam Bawah Tanah (Server Perusahaan, misal Mesin Hostinger / AWS). HTML asalnya mati statis tidak bisa berubah ubah nama akun yang login kan? PHP menyelip diantara file HTML itu untuk mencetak nyawa berdasarkan siapa yang login!

Gerbang ritual PHP dibuka dengan lambang maut: `<?php`

```html
<!-- Anggep ginian lu save bukan pake extensi .html. TAPI extensi .php! -->
<html>
    <head><title>Web Boking Tiket</title></head>
    <body>
        <h1>Selamat Datang di Pemesanan!!</h1>
        
        <!-- MEMBUKA ALAM GAIB MESIN SERVER! -->
        <?php
            // Lu bisa nyetek kode c++ style dsini
            // echo "..." adalah alat tukang cetak nya untuk dibaca sisa kode HTML bwahnya 
            echo "<p>Hari ini sisa kursi bioskop tinggal: 5 kursi dari datbass lho!</p>";
        ?>
    </body>
</html>
```
*(Catatan: Kalau kamu lihat di Browser Klik Kanan -> View Source, tulisan kode PHP nya ILANG!! Kenapa? Krn sblm dikirim k HP mu, serverya udh memproses kode itu jd tag p biasa. Jadi code PHP gak pernah bs dimaling hacker copas! Aman bgt).*

## Sang Penguasa Dolar `$` (Deklarasi Tipe Bebas)

Kalo Javascript pusing mikir `let` / `const` atau C harus *int/string*. 
Bapak PHP ini cuma butuh Uang alias Tanda Dolar (`$`) untuk menjabarkan Variabel. Tanpa tanda ini maka nilainya Error berterbagnan ga diproses.

```php
<?php
    $namaLengkap = "Toni Gnteng"; // Otomatis String
    $umur = 17; // Otomatis Int

    // Bikin kombo text sama angka yg kyak gitu gmpng? SNGT !!
    // Mirip Backtick `${}` nya JS. PHP kalo lu pakai kutip ganda ("..."), dia bisa di selipin didalmnya lgsung !!
    
    echo "Pagi bang, perkenalkan saya $namaLengkap usia saya genap $umur tahun kmarin.";
    
    // NB: Kalo ganti kutip satu ('.... saya $namaLengkap') DIA GABAKAL BISA NGASILIN NAMA TONI !! Melainkan cmn ktulis "$namaLengkap" di layar murni. Makanya PHP seru!
?>
```

Oh ya, awas!!! Jangan pernah kelupaan 1 biji nempel Titik Koma `;` di ujubg setiap kalimat print atau logic operasi di PHP. Gara gara 1 titi koma ilang, Web Hosting Lu bs mati total Blank White Screen sedih 10 juta kerugian nnti hahaha. (Tegas!)

---
[Lanjut ke Struktur Kontrol ➡️](../02-Struktur-Kontrol/README.md) | [🏠 Daftar Isi](../README.md)
