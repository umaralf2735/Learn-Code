# 04 - Fungsi di JavaScript (Pabrik Mini Andalan Kalian)

Masa kalian rela *copy-paste* kode ngitung Diskon Tokopedia 50 baris berkali-kali buat 10 barang terpisah? Tentu hal itu merusak tatanan surga kodingan. 

Disinilah hadir **Fungsi (Function)**. Fungsi adalah Pabrik Mesin Kecil yang kalian bikin sekali, dan bebas kalian pencet panggil (Call) jalankan jutaan kali.

## 1. Syntax Tradisional Tua Murni

Fungsi butuh "Corong Masukan (Parameter)" dan "Lobang Keluaran (Return)". Walau kadang juga ngk perlu.

```javascript
// 1. Memahat Fungsi Mesinnya
function kalkulatorDiskonNyepi(hargaAsli, diskonPersen) {
    let potongannya = hargaAsli * (diskonPersen / 100);
    let totalBayar = hargaAsli - potongannya;
    
    // RETURN SANGAT PENTING! 
    // Mengembalikan Uang Kembalian (Hasil) ke tangan pemanggil!!
    return totalBayar;
}

// 2. Memencet / Menghidupkan Fungsinya dgn menyetor Value ke Parameter
let tagihanAndi = kalkulatorDiskonNyepi(500000, 50); // Beli baju setengah juta, disc 50%
let tagihanTini = kalkulatorDiskonNyepi(10000, 10);  // Beli jajan wkwk

console.log("Si Andi ksuruh trnsfer: Rp." + tagihanAndi);
// Bayangkan kalian memanggil nama fungsinya doang 2 kali ga perlu ngetik kali bagi persentase lagi kan!!
```

> **Catatan Darurat Pemula**: Apa yang ada (variable) di dalam pagar perbatasan `{ }` tubuh sebuah fungsi, MAKA DIA HANYA HIDUP DISITU (`Local Scope`). Lo gaboleh iseng ngeconsole.log sebuah variable let buatan dalem fungsi dari luar fungsinya. Error karena diluar ga kenal.

## 2. Nilai Darurat Default (Menyelamatkan Website)

Sering banget *user* goblok gak masukin nilai waktu manggil fungsi (Kosong/Undefined). Supaya function mu gak memakan NaN (Not A Number) dan Error hancur, beri dia Nilai Asuransi!

```javascript
// Perhatikan namaPemesan = "Hamba Allah" (Ini nilai Backup klo kosong!)
function cetakTiketKonser(namaPemesan = "Hamba Allah", kelas = "Ekonomi") {
    console.log(`===== TIKET KONSER =====`);
    console.log(`Nama : ${namaPemesan} | VIP: ${kelas}`);
}

cetakTiketKonser("Reza Rahadian", "VVIP"); // Normal jalan normal!

// KOK DIPANGGIL KOSONG GA NGIRIM APAPA?! 
cetakTiketKonser(); // Bakal keluar output nyetak aman: Nama : Hamba Allah | VIP: Ekonomi !!!
```


## 3. Era Sintaks Modern (GGS: Ganteng Ganteng Serigala) -> *Arrow Function `=>`*

Kultur zaman NodeJS ES6 masa kini melarang penggunaan tulisan kuno `function`. Merasa kepanjangan.
Gantilah memakai simbol Panah `=>` dan disimpang dalam const.

```javascript
// Function classic:
// function pangkatDua(angka) { return angka * angka; }

// ARROW FUNCTION (Super Pendek)
const pangkatDua = (angka) => { 
    return angka * angka;
}

// LEVEL DEWA: Kalau isi kurung kurawalnya CUMA SATU BARIS DOANG DAN ITU RETURN...
// BOLEH ILANGIN SEMUA KURUNGNYA DAN KATA RETURN NYA!
const kalikanDewa = (a, b) => a * b;

console.log( kalikanDewa(5, 5) ); // 25. AJAIB KAN?
```
Itulah kenapa kalian klo magang dikantor ngeliat react isinya kode beranak panah `=>` semua! 

---
[⬅️ Sebelumnya: Array dan Object](../03-Array-dan-Object/README.md) | [Lanjut ke Algoritma Ghaib ➡️](../05-Algoritma-Dasar/README.md) | [🏠 Daftar Isi](../README.md)
