# 09 - Generics (Cawan Suci Typescript)

Bagaimana kalau kamu punya 1 fungsi kembalian, tapi kadang yang di proses itu adalah Angka Int, dan suatu hari ada yang naruh String, dan suatu hari Array? 
Masa buat `function tarikAngka`, `function tarikString` misah-misah padahal bentuk jeroannya sama?

Ini kekuatan asli TS, **Tipe Data yang Fleksibel tapi Terjaga (Generics - pakai `<T>`)**.

## Jembatan Parameter Tipe `<T>`

Kita lempar TIPENYA di depan fungsi pake kurung silang `<  >`.

```typescript
// <T> adalah wakilan "Type Apapun" yang nanti kamu pilih saat dipanggil. Kasih T aja biar singkat.
function bungkusBenda<T>(isian: T): T[] {
    // Fungsi ini akan membungkus isian mentah jadi list array!
    return [isian]; 
}

// SAAT AKU MANGGIL FUNGSI INI, AKU NGE-SET  <T> NYA SEBAGAI NUMBER:
let kadoAngka = bungkusBenda<number>(500); 
// otomatis returnya number[] -> [500]

// SAAT MANGGIL DISINI AKU MAKSA DIA TEXT:
let kadoTeks = bungkusBenda<string>("Halo Bos"); 
// otomatis returnya string[] -> ["Halo Bos"]

console.log(kadoAngka);
console.log(kadoTeks);
```

Bagi yg awam, liat syntax tipe pakai kurung panah `< >` pasti pusing. Tapi inilah pondasi Framework React dimana semua propnya dilempar secara `Generics` dibelakang layar.

---
[⬅️ Sebelumnya: Enum](../08-Enum/README.md) | [Lanjut ke Sihir Utility ➡️](../10-Utility-Types/README.md) | [🏠 Daftar Isi](../README.md)
