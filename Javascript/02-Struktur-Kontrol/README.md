# 02 - Struktur Kontrol JavaScript

Logika dasar *if-else* dan perulangan di JavaScript sangat mirip dengan struktur di bahasa standar seperti C++ atau Java. 

## 1. Percabangan dengan `if` dan `else`

Digunakan untuk memeriksa apakah suatu pernyataan bernilai `true` (benar).

```javascript
let umur = 18;

if (umur >= 18) {
    console.log("Silakan masuk, Anda sudah dewasa.");
} else if (umur >= 13) {
    console.log("Anda remaja, harus dibawah pengawasan.");
} else {
    console.log("Anak-anak dilarang masuk!");
}
```

## 2. Pengecekan Exact (Strict Equality)
Hati-Hati, sangat disarankan di javascript memakai tipe persamaan ketat (3 sama dengan) `===` daripada (2 sama dengan) `==`. Kenapa?
Karena `==` di JS suka menebak tipe data secara gaiberaturan!

```javascript
let angkaKecil = 5;      // Tipe: Number
let teksKecil = "5";     // Tipe: String

console.log(angkaKecil == teksKecil);  // Output: true (Aneh kan?)
console.log(angkaKecil === teksKecil); // Output: false (Ini lebih benar karena beda tipe!)
```

## 3. Perulangan dengan `for`

Perulangan untuk melakukan operasi berkali-kali.

```javascript
for (let i = 1; i <= 5; i++) {
    console.log(`Perulangan ke-${i}`);
}
```

Kalian juga bisa memakai loop ala While:
```javascript
let bensin = 3;

while(bensin > 0) {
    console.log("Mobil Kencang melaju!! VRoooom!");
    bensin--; // ngurangin bensin 1 liter
}
console.log("Bensin habis bosque..");
```

---
[⬅️ Sebelumnya: Dasar-Dasar](../01-Dasar-Dasar/README.md) | [Lanjut ke Array dan Object ➡️](../03-Array-dan-Object/README.md) | [🏠 Daftar Isi](../README.md)
