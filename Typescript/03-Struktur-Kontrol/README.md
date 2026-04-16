# 03 - Struktur Kontrol (Sama dengan Induk JS Semangnya)

Tidak pantas kami menyuguhkan modul beda di sini, karena pada dasarnya TypeScript (TS) mewarisi 100% gaya peredaman kendali dari Javascript ES6 aslinya.

## 1. Percabangan Bawaan

Sama persis!

```typescript
let umur: number = 21;

if (umur >= 18) {
    console.log("Diijinkan nonton bioskop malam!");
} else {
    console.log("Anak anak dilarang!");
}
```

## 2. Looping (for .. of)

Ada trik perulangan array jaman ES6 khusus Array yang lebih mentereng: `for...of` .

```typescript
let kota_raksasa: string[] = ["Jakarta", "Tokyo", "London"];

for(let kota of kota_raksasa) {
    console.log(`Turis mendarat di kota: ${kota}`);
}

// Beda ama 'in' yang mana malah ngeluarin Indeks (0,1,2, dst)
```

Gitu aja! Lanjut belajar aslinya yuk!

---
[⬅️ Sebelumnya: Annotation](../02-Type-Annotation/README.md) | [Lanjut ke Susunan Array Tuple ➡️](../04-Array-Serta-Tuple/README.md) | [🏠 Daftar Isi](../README.md)
