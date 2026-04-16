# 05 - Fungsi Berkelas Golang (Return Value Strict)

Semakin membabi-buta sebuah fungsi di JS, kamu ngga akan pernah bisa melacak sebenarnya hasil muntahan akhirnya (Yg di-*return*) itu berbentuk Teks Merah, atau Data JSON?
Jangan bikin orang yang narik fingsimu ntar pusing, BATESIN Hasil Buangannya!

## 1. Menjanjikan Hasil Return Mutlak

Berkat TS, kita kunci Tipe Data tepat setelah kurung tutup paramter! `( ... ): tipeKuncian {` !!

```typescript
// WAJIBKAN paramternya INT, dan RETtURN NYA WAjib Int!
const itungHargaKancingan = (modals: number, pajaks: number) : number => {
    let untungnyaBrp = modals * pajaks;
    
    // Kalau dibaris ini gue murtad (return "Lima Puluh Text"); TS Bakal Error Merah!
    return untungnyaBrp; 
}

console.log( "Hasil Untung Rp.", itungHargaKancingan(500, 100) ); // 500000 murni tanpa typo var!
```
Karena VSCODE udah nge-labelin ini hasil `number`. Kamu bisa langsung ngetik `.toFixed()` dst diblakng punggung pemnanggulannya! Itu sangat memanjakan developer ga perlu buang waktu debug 1 jam.

## 2. Type Void Hampa (Fungsi Mandul Beraksi Saja)

Apa bida JS murni sm C++ dan Java? Yap, disana klo Funsi cuma nyetak konsol ga punya hasil kembalian, Ditulisnya `Void`.
TS nerapin ini jg loh!!

```typescript
// Funciton Mandul ga ngasilin balikan
const menyiramTanamanMekar = (namaGeng: string): void => {
    console.log(`Menyiram kebun warga nya pak ${namaGeng} siang ini bosku..🌿`);
    
    // Disini lu dilarang keras NGETIK:  return "Selesai",
    // Kalau u iseng nge-return suatu benda, Vscode lngsung marah merah.
}

menyiramTanamanMekar("Ridwan Kamil");
```

Disadari atau tidak, TS mengubah kultur bar-bar anak Javascript menjadi ke arah *Software Maintenance* yang rapi. Orang yang pro main TypeScrpit pasti kalau belajarn **React** ato **Next.js** bakal ketagihan gara2 semua Propery Object ketebak Autocompltenya dengan lancar!!

---
[⬅️ Sebelumnya: Laci Array dan Tuple](../04-Array-Serta-Tuple/README.md) | [Lanjut ke Tahap Lanjut: Struct Interface ➡️](../06-Interface-dan-Type/README.md) | [🏠 Daftar Isi](../README.md)
