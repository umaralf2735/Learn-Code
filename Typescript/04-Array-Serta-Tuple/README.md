# 04 - Array Bertipe dan Tuple

Memasukkan data berseri. Kalau di JS kan array bisa dicampur telor+terigu+besi. Disini haram, laci besi ya laci besi, telur ya di array telur!

## 1. Array Bertipe Tunggal

Gunakan akhiran Kurung Siku Kosong `[]` diujung nama Tipenya. 

```typescript
// Aku mau membikin keranjang, TAPI KHUSUS STRING
let rakNama: string[] = ["Budi", "Andi", "Tono"];

// rakNama.push(500); // ❌ ERROR TERIAK MERAH! HARUS STRING!
rakNama.push("Joko"); // ✔️ Berhasil 

// Gimana klo array campur? Pakai Operator OR |
let laciCampur: (string | number)[] = ["Kaca", 99, 1000, "Batu"];
```

## 2. Sang Wadah Super Kaku: Tuple

Apa bedanya Tuple dan Array? Tuple itu mengatur JUMLAH SLOTNYA sekalian TIPE DATANYA BERURUTAN!
Biasanya dibuat kalau kita pengen membungkus balikan GPS (Latitude, Longitude), atau kembalian Nilai kembar.

```typescript
// BACA: Slot 0 Wajib String, Slot 1 Wajib Number, SLOTNYA MAX 2 GA LEBIH!
let KTPku: [string, number]; 

KTPku = ["Joko Ribowo", 99120];  // ✔️ Sah!

// KTPku = [99120, "Joko Ribowo"]; // ❌ ERROR!! KEBALIK URUTANNYA WEY!
// KTPku = ["Joko", 123, "Lainnya"]; // ❌ ERROR KEBABLASAN INDEX
```
Sangat keren dalam mengelola kembalian API yang bentuk kodenya sudah kita janjikan!

---
[⬅️ Sebelumnya: Struktur Kontrol](../03-Struktur-Kontrol/README.md) | [Lanjut ke Fungsi ➡️](../05-Fungsi-Type/README.md) | [🏠 Daftar Isi](../README.md)
