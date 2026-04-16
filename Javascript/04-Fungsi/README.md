# 04 - Fungsi di JavaScript

Penting untuk membungkus perintah yang sering dipakai ke dalam "Fungsi", supaya bisa dipakai ulang dengan gampang tanpa *copy-paste* berulang.

## 1. Syntax Fungsi Tradisional (Sama seperti bahasa lain)

Mirip seperti di C/Java, ini cara *classic* membuat fungsi di Javascript pakai awalan `function`.

```javascript
// Mendeklarasikan fungsi dan parameter
function hitungTotalBelanja(harga, diskon) {
    let potong = harga * (diskon/100);
    let totalBayar = harga - potong;
    
    // Memberikan uang kembalian atau hasil dari proses!
    return totalBayar;
}

// Memanggil fungsinya
let totalSaya = hitungTotalBelanja(50000, 20); // 50 ribu, diskon 20%
console.log("Yang harus saya bayar:", totalSaya); 
```

## 2. Sintaks Modern: Arrow Function `=>`

Di JavaScript versi baru (ES6), kita diberikan fitur keren untuk bikin fungsi sangat-sangat **pendek**, yang dinotasikan dengan bentuk tanda panah `=>`. Biasanya selalu disimpan ke dalam variabel tipikal konstan (`const`).

```javascript
// Function classic:
function tambahDuaAngka(a, b) {
    return a + b;
}

// ARROW FUNCTION (Tulisannya jauh lebih singkat):
const tambahPanah = (a, b) => { // tanda function dibuang, diganti panah
    return a + b;
}

// BAHKAN JIKA isinya cuma SATU baris mengembalikan nilai, bisa disingkat lagi jadi seperti ini:
const tambahPalingPanah = (a, b) => a + b;

console.log(tambahPalingPanah(5, 5)); // Output: 10
```

Arrow function seringkali bikin programmer bahasa lain kaget pertama kali liat, tapi lama-lama akan ketagihan dan ngga mau balik nulis secara tradisional!

---
[⬅️ Sebelumnya: Array dan Object](../03-Array-dan-Object/README.md) | [Lanjut ke Materi Algoritma Dasar ➡️](../05-Algoritma-Dasar/README.md) | [🏠 Daftar Isi](../README.md)
