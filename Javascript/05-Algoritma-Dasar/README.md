# 05 - Algoritma Built-in Magic (Higher Order Array)

Mengingat kalian sudah jago pakai *Arrow Function Arrow `=>`* di bab selumnya, saatnya kita mengeluarkan kesaktian JS The *Array Methods*!

Kalian tidak diwajibkan menulis manual *Bubble Sort* pakai `for` menyorong-nyorong data. Cukup pakai sihir 1 baris yang disuplai Javascript (C++ menyebut ini STL).

## 1. Penyaringan Tingkat FBI: `.filter()`

Ini dipakai untuk menjaring menyaring jutaan data berdasarkan syarat mutlak. (Hasilkan Array Kotak Baru).

```javascript
const anakAnak = [
    { nama: "Yanto", usia: 12 },
    { nama: "Bima", usia: 20 },
    { nama: "Juleha", usia: 15 },
    { nama: "Joni", usia: 25 }
];

// Misi: Tangkapin cumn orang orang DESAWSA dan Penjarakan di Array baru!!
// Cara baca (arrow filter): Muterin variabel `anakAnak`, panggil individu satuannya (orang), 
// JIKA umurnya lebih besar dari 18.. maka AMBIL dia!
const kaumDewasa = anakAnak.filter( orang => orang.usia >= 18 );

console.log(kaumDewasa); 
// AUTO NGASIH 2 ARRAY KHUSUS = [{nama:Bima}, {nama:Joni}] doang. Mantep abis!
```

## 2. Sang Petapa Metamorfosis: `.map()`

Bedanya `filter` sama `map`. Map itu NYURUH mengubah bentuk semua nilai tanpa milih milih, lalu menjadikannya array format bentuk baru! 
(Sering dipake Frontend untuk merubah List API JSON jadi list kotak Div HTML!).

```javascript
const daftarGajiOri = [1000, 3000, 5000];

// Tolong dong gw dpt bonus proyek 500 rebu per anak.. tambahin ke gajinye!
const daftarGajiBonus = daftarGajiOri.map( tagihanGaji => tagihanGaji + 500 );

console.log(daftarGajiBonus); // Jeng jeng! Keluar array baru: [1500, 3500, 5500]
```

## 3. Sort Berdarah (Mengurutkan Data Hati-Hati!)

Bawaannya `.sort()`  javascript itu NGACO. Dia menganggap semua benda adalah TEKS ALFABET ABJAD. 
Jadi kalau lu ngurutin `[2, 100, 50]` , yang juara paling depan adalah `100`. Kok bisa gitu? Iya karena menurut abjad, Huruf angka 1 (Dari Seratus) lebih awal dibanding Huruf "2". Kacau ga tuh!

**Obat Penawarnya (Mewajibkan otak Matematika Sort!):**
```javascript
let laciAngka = [30, 20, 100, 5, 2];

// Agar diurutkan sesuai matematika selisih pengurangan.
// Lu harus ngirim arrow Function yang bawa dua variable pelaga (a, b) dikurangin.
laciAngka.sort( (a, b) => a - b ); 

console.log(laciAngka); // Sempurna! -> [2, 5, 20, 30, 100]


// NB TAMBAHAN:
// Kalau kalian mau Nysun dari yg Terbesar Turun Menurun (Descending),
// Balik Saja Rumsnya Bosque!! => (b - a)
laciAngka.sort( (a, b) => b - a ); 
console.log(laciAngka); // Nggedebukk muter -> [100, 30, 20, 5, 2]
```

Tiga trinitas Dewa (`Filter, Map, Sort`) di atas akan lu gunain sampe tua bangka di perusahaan manapun lu singgah untuk *Fullstack JS Ecosystem*. Camkan baek-baek!

---
[⬅️ Sebelumnya: Fungsi](../04-Fungsi/README.md) | [Lanjut ke Keajaiban DOM ➡️](../06-DOM-Manipulasi/README.md) | [🏠 Daftar Isi](../README.md)
