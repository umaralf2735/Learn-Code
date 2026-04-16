# 01 - Dasar-Dasar TypeScript (Superset JS)

Browser Web, entah Google Chrome, Edge, dll **TIDAK MENGENAL TYPESCRIPT**. Browser HANYA kenal Javascript HTML & CSS.

Oleh karena itu, di TS kita memiliki Kompiler (Dinamakan `tsc` - Typescript Compiler). Mesin ini akan menyapu memeriksa semua "Keketatan" kodingan `.ts` mu. Jika dia tak menemukan kesalahan 1 biji pun, ia akan MENTRANSLATENYA perlahan menjadi file `.js` Murni!

## 1. Variabel Asli (Lebih dari JS)

Sama persis kayak JS lu nulisnya. Teteup pakai `let` dan `const`.

```typescript
let sapaan = "Halo Kawan, TS Nih!";
console.log(sapaan);
```

Bedanya, coba tulis di baris bawahnya:
```typescript
let sapaan = "Halo Kawan!";
// Di JS biasa baris ini akan aman dan tembus ke browser.
// TAPI DI TS INI ERROR KEMUMERAH DAN GAK BISA DISAVE (COMPILATION ERROR)!
// "Cannot assign to 'number' because its type string at birth"
sapaan = 90; 
```

Disinilah para Developer raksasa sedunia sujud pada TypeScript. Ia membunuh error "konyol ubah tipe (NaN)" ratusan jam sebelum itu masuk ke layarnya user!

---
[Lanjut ke Pembatas Annotation ➡️](../02-Type-Annotation/README.md) | [🏠 Daftar Isi](../README.md)
