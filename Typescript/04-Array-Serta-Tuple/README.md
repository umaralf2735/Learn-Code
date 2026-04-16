# 04 - Menyucikan Array dan Merakit Tuple

Array (kardus Laci data) di Javascript sangat kotor nyampur ga jleas. Lo bisa nyimpen Baju, Garpu, sama Ban Mobil di Array Loker yang sama kan di JS. Itu rentan merusak perhitungan di loop nanti loh.

TS memaksa lu: Rak Buku ya Rak Buku! Harus murni String smua!

## 1. Array Bertipe Murni Tunggal

Supaya Suci murni, Berikan Label tipe dikuit kurung siku kosong `[]`.

```typescript
// Laci ini HARAM hukumnya kemasukan angka!!!
let rakSenapanList: string[] = ["Sniper", "Pistol", "Senapan Angin"];

// rakSenapanList.push(5000); 
// ❌ ERROR TERIAK MERAH! HARUS STRING BOS WALAUPUN LU PUSH!

rakSenapanList.push("Pelontar Rocket"); // ✔️ Berhasil 

// ❓ Gimana bang kalo gue kepaksa nyampur? (Gunakan Kurung | Or Pipa Panjang Lgi)
let laciPasarGila: (string | number)[] = ["Kaca", 99, 1000, "Baju Bekas", 0];
```

## 2. Sang Wadah Super Kaku & Mutlak: Tuple

Apa bedanya Tuple dan Array? Array itu Jumlah panjang lsicnya bisa namba melar dari 3 barang ke sejuta barang.
Tuple itu **MENGUNCI JUMLAH SLOTNYANG TERSEDIA** DAN **TIPE NYA HARUS BERURURAN MURNI!!** 

Kapan hal alien ini dipake?
Coba Inget Google MAPS Kordinat, cuman btuh DUA SLOT kan? Satu String, satu Angka!

```typescript
// BACA ALUR TS INI: Slot ke-0 nya WAJIB String, Slot ke-1 WAJIB Number, SLOTNYA MAXIMAL CUMAN 2 GA LEBIH!
let kordinatPetaGPS: [string, number]; 

// Masukin data pake array biasa
kordinatPetaGPS = ["Ujung Kutub Utara", 99120];  // ✔️ Sah!

kordinatPetaGPS = [99120, "Kutub"]; 
// ❌ ERROR!! KEBALIK URUTANNYA WEY HARUS STRING DLU TRS ANGKA WKWK!

kordinatPetaGPS = ["Ujung", 123, "Lainnya"]; 
// ❌ ERROR KEBABLASAN !! SLOT KAMU MNTA NYA MNTOK 2 DOANG !!
```
Tuple adalah tameng paling tebal bagi programer untuk membaca kembalian Data API Sensor yg sudah mutlak urutannya misal `[ "Suhu 32C", true, 90 ]` ga bsa diganggu gugat ukurannya.

---
[⬅️ Sebelumnya: Struktur Kontrol Basic](../03-Struktur-Kontrol/README.md) | [Lanjut ke Fungsi Sakral ➡️](../05-Fungsi-Type/README.md) | [🏠 Daftar Isi](../README.md)
