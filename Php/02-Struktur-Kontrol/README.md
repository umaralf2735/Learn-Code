# 02 - Struktur Kontrol PHP (Aliran Logika Standar Murni)

Materi disini gak akan bertele tele pusing. Kenapa? Karena **PHP itu 100% fotocopy anak kembar identik dari Javascript/C+** di soal penulisan Alur Perulangan!

Kalian tidak butuh pusing ngapalin Indentasi kaya Python ato panah panah aneh. Semuanya kurung Kurawal tua baku klasik `{ }`!

## 1. If / Else
Syaratnya harus dimasukkan dlm Kurung Melengkung `()`, baru dikasih badan kurawal.  Beda dgn JS `else if` dipisah, di php mreka gnyatu jadi satu kata `elseif`! 

```php
<?php
    $saldoKu = 12000;

    if ($saldoKu >= 50000) {
        echo "Wow, uang banyak, makan mcd gan!";
    } elseif ($saldoKu >= 10000) {
        echo "Cukup beli mie rebus indomie di warkop.";
    } else {
        echo "Aduh.. kudu utang ibu kost dah..";
    }
?>
```

## 2. Looping For (Untuk Nampilin Tabel Tagihan!)

Bayangin klo bos u nyurh ngeluarin struk 50 Tagihan di tabel HTML, gak usah dicopas HTML tag nya bang 50 kli, Pake PHP!! 
*Peringatan: perhtiin penyambung text nya bkn Tanda Plus ( + ), tapi Tanda Titik!! (`.`)*

```php
<table border="1">
    <tr>
        <th>Nomer Urut Tagihan</th>
    </tr>
    
    <?php
    // Inisiasi (Keluarkam $i = 1) ; Selama kurang dr 6 ; Naikin terus 1 !
    for ($i = 1; $i <= 5; $i++) {
        
        // Cetak tag Pembungkus baris tabel <tr> di cmpur angka urutannya wkwk!
        echo "<tr> <td>Ini data pesanan nomor ke-" . $i . "</td> </tr>"; 
        
    }
    ?>
    
</table>
```
Kalo di Save File atasnya jd `.php` lalu d run dari dalem `XAMPP localhost`. JENG JENG!! Jadilah tabel struk pembayaran Tokped buatanmu!!! Begitulah rahasianya broo! 

---
[⬅️ Sebelumnya: Dasar-Dasar Tulis HTML](../01-Dasar-Dasar/README.md) | [Lanjut ke Dictionary Map Array PHP ➡️](../03-Array-Assosiatif/README.md) | [🏠 Daftar Isi](../README.md)
