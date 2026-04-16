# 10 - Jantung Proyek TypeScript (`tsconfig.json`)

Kamu sudah pelajari 9 bab bahwa File TS itu gbsa di baca di Chrome/Web, karena browser cuma kenalnynya JS kuno telanjang murni.
Maka kalian make Tukang ketik komliasi `tsc filemu.ts` untuk ngerubahin 1 btih fike itu kan di bab 1?

Gimanan carny kalo kalian pnya Folder Projak besar yg iinya ratusan ribu file `.ts` bersarakan? Masa mo ketik 1 per satu tsc nama file nya ??
Masuklah file Ajaibb Pussat Kendali Mesin : `tsconfig.json`.

## 1. Memanggil Buku Kitab Proyek

Ketik ini di terminal pada saat kamu pmbikin foolder Proyekmu baru prtmaa kali wkt perawan:

```bash
tsc --init
```

Seketika file ghaib brnama `tsconfig.json` trn lgsg ada. Klo lu buka file ini isinnya panjng gajelas bynk komentar Ijo Ijo... 
Tenang.. Kunci intiny cuman dikitt yg perlu diubah.

## 2. Settingan Rahasia Menjadi Developer Pro
Buka tsconfig lu dan cari/ubah tulsiab inni jdi kyk diabwH:

```json
{
  "compilerOptions": {
      
    // 🌟 MENTUJU VERSI ECMASCRPIOT BRAPA HASIL KOMPLIASU LU NNTI NYA JADI (.js) NYA ??   
    // Klo elu ketik ES6/ES2015.. Nnti const / lety kmu tetwp aammamn. 
    // Tpi klo targetnya ES3, NNTi Const Lu di JS asliny Bkl brubah sendiir smua jd "var" hahah agar bsa dipake di Inettnerxploreer kakek kake!!
    "target": "ES6", 
    
    // 🌟 LOKASI TEMPAT BUANGAN HASIL FILE .JS NYA! 
    // Biar gak campur brebtanakan sama file aslu TS nya didlem fodernya kan risih liatny..
    // Kta bikin folder build / dist bwr ngumpul disitu dlm keadaam trpisah!
    "outDir": "./dist",
    
    // 🌟 PENGAMANN PALING KETTATT DI DUNIIAAA ("HARUS MENYALA!!! TRUE")
    "strict": true,
    
  },
  
  // 🌟 FOKLDEER MANA YG MAAU DIJAGAIN/ DI COMPOLASI SAMA MESIN ININ ??
  "include": ["src/**/*"]
}
```

## 3. Mantra Putar Pabrik Sekali Klik !
Sekarag.. Klaina  tinggal bikin file file dsar mu simpen aja di dlaem fodler `src`. 
Kalao klaian mau merubah file itu jdi Javascript.. **KALIAN GAUSHA NGETK NMA FIlENYA LAGI!**

CUKUP TEKAN/KETK DIM TERMINAL:
```bash
tsc 
```

BAM! Semua isIaan fder `src` lo yang berupaa ribuna file `.ts` BAkaalan lgsng Disaring dicompoiler ke dalam Filder baru benama `/dist/App.js` ... dll secara mssal !!!

Tamatlah riwayat Pelajrn TypeScript ini! Skrg u udh setara dengan mid-level React Devlopers diluar sana yang sudah menharamkan penggunaan JS Murni di perusahaanya. Maju trs TS!!!

---
[⬅️ Sebelumnya: Generoiks Magic Type](../09-Generics/README.md) | [🏠 Daftar Isi Utama TypeScript](../README.md)
