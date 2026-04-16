# 03 - Struktur Kontrol dan Perulangan  (Kembaran Javascript Murni)

Materi disini beneran identik sama JS ES6 tanpa basa basi. Tentu dong, karena TypeScript ya Javascript jg sbenrnya tapi di strict in.

## 1. Percabangan Bawaan Strict

Bedany, kalian gak usah takut klo ada org gila ngirimin Angka Umur tapi bentuknya String `"21"`. Gak usah repot ngetik sama-dgn-3 (`===`) lagi buat bedain String sm Number. Di Tipe Annotation TypeSript sejak var diciptain udh dibatesin Type number pastinya.

```typescript
// Aman mutlak krn ini brrrti cumn Nrima Angka asli
let umurKlienTamu: number = 21;

if (umurKlienTamu >= 18) {
    console.log("Kasih pesenan Kopi Hitam Dewasa!");
} else {
    console.log("Kasih adeknya sirup coco pandan!!");
}
```

## 2. Looping (Harta Karun `for .. of`)

Kalian mau muterin sebuah Array? Daripda mumet nulis indeks `[0], [1]` mending pake jalan pinter `for of`. Ini jalan yang sangaaaaaat bnyk dipake d Frontend.

```typescript
// Memaht array kudu paje Kurung Siku Kosong blkngnya!
let kota_raksasa_indo: string[] = ["Jakarta", "Surabaya", "Medan"];

// KITA CARI TAU ISINYA SEMUA!! ("Puterin bro! Pindahin masing2 ke var xkota sementara!")
for(let xkota of kota_raksasa_indo) {
    
    // xkota langsung isisnya "Surbaya!" Bukn 0 atatu 1 indexnya!!
    console.log(`Turis mendarat di kota: ${xkota}`);
}

/* 
AWAS JANGAN KETUKER AMA JS KUNO PUNYA YA (for .. IN). 
Kalau lu tulis IN: Lu malah dapetin index angkanya (0, 1, 2) BUKAN NAMA KOTANYA! wkwk.
*/
```

Itu aja! Gampang bgt kan ngendalin alurnya di TS.

---
[⬅️ Sebelumnya: Type Annotation Cap Label](../02-Type-Annotation/README.md) | [Lanjut ke Susunan Array Tuple Sakti ➡️](../04-Array-Serta-Tuple/README.md) | [🏠 Daftar Isi](../README.md)
