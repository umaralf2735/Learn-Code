# 02 - Struktur Kontrol & Perulangan (Otak Sang Aplikasi)

Sebuah kode JS yang lurus dari atas ke bawah itu membosankan. Komputer baru terlihat cerdas kalau dia bisa "mengambil keputusan milih cabang jalan" dan "melakukan tugas capek berulang-ulang". Itulah kegunaan bab ini.

## 1. Percabangan dengan `if` dan `else`

Digunakan untuk memeriksa dan membelah jalanan logika. Mesin akan ngecek di dalam kurung `()` apakah itu `true`. Kalau iya, kurung kurawal `{}` dijalankan. Kalau bohong (`false`), dia lompat ke jurang `else`.

```javascript
let bensinMobil = 1; // Liter

if (bensinMobil >= 10) {
    console.log("Tancap gas luar kota gan!");
} else if (bensinMobil >= 3) {
    console.log("Cukup muter-muter alun alun aja lah.");
} else { // SISA TERAKHIR JIKA KONDISI DIATAS GA ADA YG KEPILIH
    console.log("Mogok woy. Cari kang eceran cepetan.");
}
```

## 2. Awas Penyakit Javascript: `==` VS `===` (PENTING!)

Ini adalah **pertanyaan Wawancara Kerja paling mematikan** bagi programmer web.
Kalian wajib menggunakan 3 biji sama dengan (`===`) untuk mengecek kesamaan di JS. JANGAN mendua (`==`). Kenapa? Karena JS suka menerka-nerka (*Type Coercion*).

```javascript
let umurAnak = 17;      // Tipe: NUMBER Asli
let umurAnakPalsu = "17"; // Tipe: STRING (Tapi isinya mirip angka)

// ❌ DOSA BESAR (Kurang Ketat)
console.log(umurAnak == umurAnakPalsu); 
// Output: TRUE! Wah bahaya, padahal beda tipe! JS otomatis manupulasi mereka setara tipe.

// ✔️ CARA DEWA (Strict Equality)
console.log(umurAnak === umurAnakPalsu); 
// Output: FALSE! Mesin Cerdas! Dia nolak karena biarpun angkanya 17, yang satu Nomor yang satu Text huruf!
```

## 3. Truthy & Falsy (Hantu di JS)
Dalam kurungan `if`, JS kadang menaruh kecurigaan. Kalau elo ngecek sebuah var yang isinya Angka Nol `0` atau String Kosong `""`, JS otomatis menganggap mereka `false`!

```javascript
let namaDicari = ""; // Kosong ga diketik

// JS akan merubah "" otomatis mnjd false di dalam if()!
if (namaDicari) {
    console.log("Nama ditemukan loh: ", namaDicari);
} else {
    console.log("Hayo lu belum ngisi form nya mas bro!");
}
```
*Trik ini sering dipake buat nge-validasi input form kosong/nggak looh.*

## 4. Perulangan (Looping)

Misal bos kalian nyuruh nyetak tulisan 100 kali. Kalau kalian *copas* console.log seratus kali, kalian mending gaperlu jadi programmer. Komputer diciptakan buat tugas perulangan (*Iteration*).

### A. FOR Loop (Jelas Batasnya)
```javascript
// Mulai dari i = 1; Muter selama i kurang/sama dengan 5; i nambah sendiri pelan pelan
for (let i = 1; i <= 5; i++) {
    console.log(`Bocah lari muterin lapangan putaran ke-${i}`);
}
```

### B. WHILE Loop (Nunggu Sampai Ketemu Batas Gaib)
Kalo elo gatau kapan selesainya programnya, pake ini sampe batasnya kepicu dari dalem program.

```javascript
let uangGajian = 50; // Ribu
let hargaKopi = 15; // Ribu

while (uangGajian >= hargaKopi) {
    console.log("Asikk nyeduh kopi nangkring di cafe..");
    uangGajian -= hargaKopi; // Uangnya pelan pelan tekor disunat 15rb
}
console.log(`Haduh sisa uangku cuman ${uangGajian} ribu ga cukup ngopi. Plg ah.`);
```

---
[⬅️ Sebelumnya: Dasar-Dasar](../01-Dasar-Dasar/README.md) | [Lanjut ke Array & Object ➡️](../03-Array-dan-Object/README.md) | [🏠 Daftar Isi](../README.md)
