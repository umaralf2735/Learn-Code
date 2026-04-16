# 01 - Dasar-Dasar TypeScript (Perisai Pelindung JS)

Sering denger kata TypeScript (TS)? Ini bukanlah bahasa pemrograman baru yang musuhan sama Javascript. 

Ibaratnya JS itu orang telanjang yang bebas lari sana-sini. Nah, TypeScript ini adalah **Baju Zirah (Baju Besi Pelindung)** yang dipakein ke orang tersebut. Biar dia jalannya lebih terarah dan ga gampang mati luka kena pedang (Error).

TS diciptakan oleh *Microsoft* karena programmer sedunia pusing nyariin Bug error di JS yang kadang muncul tiba-tiba gara-gara Tipe Data nya bisa keliru.

## 1. Kompilasi (Menerjemahkan ke Dunia Nyata)

Browser Chrome, Firefox, dkk **TIDAK BISA MEMBACA TYPESCRIPT**. Mesin-mesin itu cuma kenal HTML, CSS, dan murni JS Vanila.

Lalu gimana kodingan TS kita jalan dong? Kita pake "Tukang Terjemah" bernama Compiler (`tsc`). 
Semua file `.ts` murni kalian akan *disapu, diperiksa keketatannya*, lalu kalau gaada error, MESIN BAKAL MENGKLONINGNYA JADI FILE `.js` Murni!

```bash
# Kamu ngetik di TS :
tsc file_utamaku.ts 

# BIM SALABIM! Tiba tiba muncul file baru 'file_utamaku.js' disebelahnya
# yang bs masuk di taruh browser!
```

## 2. Pagar Ketat Variabel 

Ngetiknya sama persis JS, pake `let` dan `const`. TAPI... TS ini pemarah kalat typenya dilecehkan.

```typescript
// Anggap kita ngoding di JS biasa:
let duitTunjangan = 500;
duitTunjangan = "Gajadi Cair Bulan Ini"; // Diubah mendadak dr Angka ke Teks?!
// ☝️ DI JS KUNO: AMAN JAYA LANJUT JALAN GA ADA ERROR! 

// 🌟 NAH DI TYPESCRIPT: (ERROR MELEDAK!)
// "Bro, sejak awal dia angka, gila aja lu tiba-tiba timpa jd Text huruf! Ga bisa disave!"
```

Disinilah para Developer Raksasa sedunia bernafas lega. TypeScript **Membunuh error konyol ratusan jam SBLOM ITU NAIK KE produksi MATA USER!** Kamu akan dipaksa rapi sama TS layaknya pake Bahasa Bapaknya C++ murni!

---
[Lanjut ke Sabuk Pengaman: Type Annotation ➡️](../02-Type-Annotation/README.md) | [🏠 Daftar Isi](../README.md)
