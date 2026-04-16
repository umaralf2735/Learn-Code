# 02 - Type Annotation (Memberi Label)

Selain mengandalkan ketajaman batin TS menebak (Inference). Kita selayaknya pendekar harus melabeli paksa setiap variabel baru dengan `Titik Dua : namaTipe`.

## Tipe Dasar

Sama semua macem si JS. Ada string, number, bool, any (Bebas).

```typescript
// Memaksa bahwa ini SELAMANYA Angka
let hargabarang: number = 25000;

// Memaksa tipe selamanya text
let tulisan_pujian: string = "Wah hebat banget lu!!"; 

// Memaksa Boolean
let apakahMenang: boolean = false;
```

## Tipe `any` (Dihindari/Haram)

Saking strictnya, kadang programmer nangis merengek ingin memasukkan data bebas apapun layak JS kuno. Diciptakannlah `any`.

```typescript
let misteri: any = "Bisa jadi tulisan";
misteri = 900;     // Aman (dianggap int)
misteri = false;   // Aman
```
Tapi **JANGAN PERNAH PAKE ANY** Kalau ngga kepaksa mentok gatau data dr internet bentuknya apa! Pakai any membuat TS mu tak ada gunanya dan berwujud JS biasa lagi ahaha.

---
[⬅️ Sebelumnya: Dasar-Dasar](../01-Dasar-Dasar/README.md) | [Lanjut ke Struktur Kontrol ➡️](../03-Struktur-Kontrol/README.md) | [🏠 Daftar Isi](../README.md)
