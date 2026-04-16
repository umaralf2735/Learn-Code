# 01 - Dasar-Dasar JavaScript

Halo! Selamat datang di modul pertama JavaScript. Tidak seperti bahasa lain yang butuh proses *compile*, JavaScript bisa langsung dijalankan di *browser* kamu (Chrome, Firefox, dll) atau menggunakan sistem Node.js di komputer.

## 1. Menampilkan Sesuatu (Output)

Di JS, cara paling umum untuk mengecek hasil dari kodemu adalah dengan mencetaknya ke konsol (*Console*).

```javascript
// Akan mencetak teks ini di terminal atau console browser
console.log("Hello, World!");
console.log(100 + 50); // Bisa langsung menghitung angka
```

## 2. Variabel (`let`, `const`, dan `var`)

Di JS aslinya dulu kita memakai `var` untuk menyimpan data. Tapi sekarang (Modern JS), SANGAT DISARANKAN untuk hanya memakai `let` atau `const`.

### `let` untuk data yang bisa berubah (Variable)
```javascript
let nama = "Budi";
console.log("Nama saya:", nama);

// Mengubah isi variabel nama
nama = "Andi"; 
console.log("Sekarang jadi:", nama);
```

### `const` untuk data tetap (Constant)
Sama seperti `const` di Golang, nilainya tak bisa diganti.
```javascript
const phi = 3.14;
console.log("Nilai Phi:", phi);

// phi = 3.15; // INI AKAN ERROR!! karena const tidak bisa ditimpa
```

## 3. Tipe Data Dasar

JavaScript adalah bahasa yang tipe datanya sangat fleksibel (tidak perlu ditulis int atau string saat deklarasi, si JS pintar menebak sendiri).

- **Number**: Angka berapapun entah desimal atau bulat. (contoh: `10`, `3.14`)
- **String**: Teks, dibungkus dengan petik ganda `""`, tunggal `''`, atau backtick ` \` \` `.
- **Boolean**: Jawaban benar `true` atau salah `false`.
- **Undefined**: Variabel yang sudah dibuat tapi belum dikasih nilai apa-apa.
- **Null**: Secara spesifik kita beri tahu variabelnya bahwa isinya "KOSONG/Hampa".

```javascript
// Contoh tipe data String menggunakan tipe backtick (Template Literal)
let sapaan = `Halo, nama saya ${nama}!`; 
console.log(sapaan);
```

---
[Lanjut ke Materi Struktur Kontrol ➡️](../02-Struktur-Kontrol/README.md) | [🏠 Daftar Isi](../README.md)
