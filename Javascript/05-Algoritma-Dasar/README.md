# 05 - Algoritma Dasar (Built-in Magic)

Sejujurnya saat kita memakai JavaScript, sangat jarang kita akan menulis sebuah algoritma dari dasar (*scratch*) seperti `Bubble Sort` atau `Linear Search` menggunakan *loop* ganda. Kenapa? Karena di JavaScript, Array sudah dibekali "kekuatan sakti" berupa *Built-in Method*.

## 1. Searching (Pencarian)

Dibanding meloop manual satu satu mencari benda, pakai saja method Array super canggih bawaan JS!

### Menggunakan `find()`
Cocok dipakai untuk mencari data di dalam "Array yang isinya Object" dengan kriteria spesial kita sendiri.

```javascript
let murid = [
    { nama: "Yanto", nilai: 60 },
    { nama: "Bima", nilai: 90 },
    { nama: "Juleha", nilai: 85 }
];

// Kita mencari SIAPA yang nilainya 90?
// Menggunakan Arrow Function untuk mencari dari daftar:
let anakPintar = murid.find( orang => orang.nilai === 90 );

console.log("Ketemu!", anakPintar.nama); // Bima
```

### Menggunakan `includes()`
Bermanfaat jika hanya menanya keberadaan "ADA/TIDAK ADA" sesuatu yang simpel. 

```javascript
let keranjangJajan = ["Biskuit", "Susu", "Coklat"];

let adaSusuNggak = keranjangJajan.includes("Susu"); // true
let adaRotiNggak = keranjangJajan.includes("Roti"); // false

console.log("Apakah ada susu?", adaSusuNggak);
```

## 2. Sorting (Pengurutan)

JavaScript memiliki `sort()`. Namun **Hati-Hati!!** By default (secara bawaan), JS mengurutkan data dengan menganggap **semuanya sebagai teks (String)**.

```javascript
let laciAngka = [30, 20, 100, 5, 2];

// Kalau di-sort polos...
laciAngka.sort();
console.log(laciAngka); 
// Output: [100, 2, 20, 30, 5] --> SALAH SECARA MATEMATIKA!! KARENA DIURUTKAN SECARA ABJAD AWAL!
```

### Cara Sort Angka yang Cerdas
Kita harus beri *Arrow function* rahasia agar JS membedakan ukurannya dengan angka:

```javascript
let laciAngka = [30, 20, 100, 5, 2];

// Agar diurutkan sesuai matematika, kita beri tau cara menyortirnya: (a - b)
laciAngka.sort( (a, b) => a - b ); 

console.log(laciAngka); // [2, 5, 20, 30, 100] -> MANTAPP!
```

Keliatan kan bedanya? Di Golang kalian nulis Bubble Sort panjang-panjang, di JS cukup satu baris kalau tau nama jurusnya!

---
[⬅️ Sebelumnya: Fungsi](../04-Fungsi/README.md) | [Lanjut ke Materi DOM ➡️](../06-DOM-Manipulasi/README.md) | [🏠 Daftar Isi](../README.md)
