# 06 - Cetakan Objek (Interface & Type)

Saat kita menarik data panjang JSON dari Internet (`fetch`), si Javascript cuma nerima buta anggap itu Object mentah. Tapi TS gak mau nerima kalau kamu tidak menyediakan "Struct / Structur Blueprint" buat wadah tangkapannya!

Kita gunakan **Interface** (atau `type`).

## Mendeportasi Dosa ke Interface!

Bila C punya Struct, TS murni menyebutnya Interface (Antarmuka Kontrak). 

```typescript
// Bikin kontrak mati bahwa setiap 'Senjata' wajib punya hal berikut:
interface Senjata {
    namaBenda: string;
    dayaHancur: number;
    // Pake tanda tanya '?' artinya Boleh Ada Boleh KOSONG (Optional/Undefined)
    punyaRacun?: boolean; 
}

// Bikin satu buah objek js Murni, tapi di "CAP / DIKUNCI" kedalam interface Senjata
const pedangSakti: Senjata = {
    namaBenda: "Excalibur",
    dayaHancur: 999
    // Gapapa aku ga nulis punyaRacun, soalnya ada tanda ? 
};

// KALAU KITA ISI NGASAL GINI AUTO ERROR SEBELUM DI COMPILER!
// const tameng: Senjata = {
//     pertahanan: 100 // ❌ ERRROR!! GAADA DI KONTRAK INTERFACE SENJATA TAHU!
// }
```

Inilah rahasia Developer Frontend React.js selalu bebas bug error typo. Karena begitu mereka ngetik `pedangSakti.` , si VSCODE langsung nampilin Autocomplete `namaBenda` persis hasil bacaan Interfacenya! Gak mungkin Typo huruf haha hihi.

---
[⬅️ Sebelumnya: Fungsi](../05-Fungsi-Type/README.md) | [Lanjut ke Class OOP ➡️](../07-Class-OOP-Strict/README.md) | [🏠 Daftar Isi](../README.md)
