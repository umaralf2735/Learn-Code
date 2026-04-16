# 02 - Type Annotation (Memberi Cap Lebel Type)

Daripada ngandelin TS nebak pusing sendiri, kita selayaknya Pendekar Pedang harus mencap (Annotation) semua Variabel saat dia diciptakan biar aman dari Typo!

Rumusnya: Kasih titik dua dan nama tipenya -> `: string` di samping kanan Variabel lu.

## 1. Tipe-Tipe Dasar TS

Coba liat keketatan pemahatan variabel dsini:

```typescript
// MEMAHAT BAHWA INI SELAMANYA BEISI ANGKA (Int / desimal bs bebas)
let totalPelanggan: number = 75000;

// Memaht TEXT (Wajib pakai kutip)
let cuitanTwitter: string = "Wah pemilu kmarin seru amat bosque!"; 

// Memahat Logika Saklar (Hnya false / true mutlak)
let bapakSedangPulang: boolean = false;
```

Begitu kamu ketik kayak diatas. Otak VSCODE (Text Editormu) bakan **ngintilin** lu!! 
Misal lu ngetik `totalPelanggan.` -> Vscode auto ngluarin alat alat pertukangan khusus ngitung matematika doank!! Gak ada alat alat String disitu. Inilah mantapnya Autocomplete TS.

## 2. Sang Hantu Kegagalan TS (`any`)

Saking ketatnya C-Sharp dan Java... Programmer FrontEnd yg dari dulu dimanja ama kebabasan JS suka meraung-raung meronta kepusingan pake TypeScript.

Maka Microsoft nyiapin lobang Tikus pelarian: **Tipe `any` (Alias Tipe Apapun Boleh Nabrak Kek JS Kuno)**.

```typescript
// Membuka segel iblis!! (Mending gausa di anotaisn lo kl ujuny any)
let misteriKereta: any = "Kereta ini bs jd text";

misteriKereta = 900;       // ✔️ Aman nembus (dianggap int)
misteriKereta = false;     // ✔️ Aman jg diganti bool...
```

**⚠️ PERINGATAN KERAS PERUSAHAAN!!**
Di kantoran.. elu ngetik Any 1 kali, Senior elu bisa nyoret merah nendang lu dari perkejaan!! ANY HANYA BOLEH dipakai sesaat kalalu Lita BENAR BENAR BINGUNG hasil Sedotan JSON database dari Web Cina Asing luar gatau bentuk datnya apa! Hindari ANY Sebisa Mungkin!

---
[⬅️ Sebelumnya: Dasar-Dasar VS JS](../01-Dasar-Dasar/README.md) | [Lanjut ke Struktur Kontrol ➡️](../03-Struktur-Kontrol/README.md) | [🏠 Daftar Isi](../README.md)
