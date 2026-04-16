# 01 - Dasar-Dasar JavaScript (Gerbang Dunia Web)

Halo! Selamat datang di modul pertama JavaScript. Tidak seperti bahasa lain (C++ atau Java) yang butuh proses *compile* rumit berjam-jam, JavaScript adalah bahasa penurut yang bisa **langsung dijalankan** saat ini juga di *Browser* kamu (Chrome, Firefox, Safari) atau menggunakan sistem Node.js di komputer.

## 1. Menampilkan Bukti Kehidupan (Print / Output)

Di bahasa pemrograman manapun, hal pertama yang harus kita kuasai adalah menyuruh komputernya ngomong. Di JS, tempat ngomongnya itu tersembunyi di konsol (*Console*).

*Coba buka Chrome, tekan F12, cari tab tulisan Console, lalu copas kode ini:*
```javascript
// console.log() adalah fungsi paling sering diketik programmer seumur hidupnya.
console.log("Hello, World! Ini program JS pertama saya!");

// JS pintar matematika dasar:
console.log(100 + 50); // Output: 150

// Kalo lagi nge-debug aplikasi yg gagal, pakai alarm ini biar merah:
console.error("ALARM: Internet Putus Woi!");

// Kalo mau sok pro, tampilkan data seperti tabel excel:
console.table(["Mangga", "Apel", "Jeruk"]);
```

## 2. Variabel: Mengotakkan Data (`let`, `const`, dan Kakek `var`)

Variabel itu **ibarat ember plasik**. Kamu bisa naruh air (data) di ember itu, trus nempel label kertas diatasnya (nama embernya).

Di JS zaman jebot, orang-orang numpahin air ke ember pakai kata `var`. Tapi ini **SANGAT BERBAHAYA DAN BIKIN BUG**, karena `var` itu bocor (Bisa diakses dari luar pagar rumah/scope). Maka dari itu di Modern JS, **Haramkan mengeik `var`**. Gantilah dengan `let` atau `const`.

### A. `let` (Ember yang Airnya Bisa Diganti)
```javascript
// Bikin ember namanya 'skorPlayer'
let skorPlayer = 50;
console.log("Mula mula skornya:", skorPlayer);

// Di pertengahan game, skornya nambah!
skorPlayer = 100; // Tinggal timpa ulang
console.log("Wah sekarang dapet:", skorPlayer);
```

### B. `const` (Kotak Brankas Baja Permanen)
Ini sangat dianjurkan kalau data yang kamu simpan itu hukumnya WAJIB tetap & tak tergoyahkan (Misal nomor KTP, atau nilai gravitas bumi).

```javascript
const NAMA_DEWA = "Zeus";
console.log("Sesembahannya adalah:", NAMA_DEWA);

// JIKA NEKAT DIGANTI:
// NAMA_DEWA = "Hades"; 
// ❌ ERROR MERA MERONA!! (TypeError: Assignment to constant variable).
```
> **Tips Pro:** Sebisa mungkin selalu pakailah `const` di awal ngoding! Ubahlah jadi `let` HANYA JIKA nantinya variabel itu dipaksa berubah harganya.

## 3. Tipe Data Fleksibel Ala Ninjutsu

JS itu punya sistem "Ketik Dinamis". Kamu nggak perlu koar-koar ke memori bilanh "WOI INI ANGKA LHO YAA". JS cuman ngangguk dan otomatis nebak isinya sendiri.

- **Number**: Angka bulet (`10`) atau desimal / pecahan koma (`3.14`). Semua dianggep sama.
- **String**: Teks curhatan. Selalu wajib diborgol oleh Petik Ganda `".."`, Tunggal `'..'`, atau *Backtick* `` `..` ``.
- **Boolean**: Saklar On/Off. Tipenya cuma dua makhluk aja: `true` atau `false`.

```javascript
let musuhMati = false; // Tipe Boolean

// 🌟 MAGIC OF MODERN JS: TEMPLATE LITERAL (Backtick)
let nama = "Ridwan";
let duit = 5000;

// Daripada kamu nyambung string capek2 gini = "Halo " + nama + " duitmu " + duit
// PAKAI BACKTICK! Angka dollar ${} langsung menarik masuk variabel ke dalam text!!
let sapaanLebay = `HALOW BOSSKU ${nama}!! Widih duitnya sisa Rp.${duit} nih ye!`;

console.log(sapaanLebay);
```

---
[Lanjut ke Materi Struktur Kontrol ➡️](../02-Struktur-Kontrol/README.md) | [🏠 Daftar Isi](../README.md)
