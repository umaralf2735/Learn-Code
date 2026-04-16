# 06 - Interface dan Type (Memborgol Objek Ghaib JSON)

Bila di Arrays kita udah diajarin ngeborgolnya pake `string[]`. Gimana ceritanya klo ada OBJEK BESAR NYA JAVASCRIPT kaya misal data `Response API Profil Pasien RS`?

Kan isi object nya campur aduk: Ada yang angkanya umur, ada String untuk namaPasien, daan boolean untuk idupMati nya!
Disinilah senjata terpadu **`Interface`** dan **`Type`** beraksi. Lu bisa nyetak "Cetakan Template" ghoib pelindungnya TS!

## 1. Cetakan `interface`

Sangat bagus digunakan saat merancang Objek di Aplikasi gede yang banyak turunannya kayak Angular.

```typescript
// Bikin Cetakan Pintu Masuk! 
//(HURUF DEPAN WAJIB BESAR YA SOALNY INI TEMPLATE, BKN VARIABEL!)
interface WargaNegara {
    noIdentitas: number;
    namaResmi: string;
    sudahMenikah: boolean;
    // Tnda Tanya '?' berarti Opsional: (Kalo dia ga ngisiin umur ga bkalan Error TS nya!!)
    umur?: number; 
}


// SAATNYA MENGGUNAKAN BAJU ZIRAH INI KE VARIABLE OBJECT KITA:
// Perhtikan tnda titikduahnya WargaNegara :
let pakDidi: WargaNegara = {
    noIdentitas: 1234567,
    namaResmi: "Raden Didi Sucipto",
    sudahMenikah: true
    // Uumur gak di cantumin gpp soalna ada tnda (?:)
};

// PAKSAAN TS MURNI!:
// Kalo eelo iseng ngeganti pakDidi.sudahMenikah = "Belum Mas Bngttt"; (STRING). ERROR PASTI!! Krn mintanay boolean!
```

## 2. Cetakan `type` Alias (Jurus Kembar Pilihan)

Apa bedan intferface sm type? Kalo Type biasnaya lebih "Fleksibel Custom" untuk pilihan yg mutlak cuman bbrp kata aja!

```typescript
// Memahta cumn nrima dua buah kata inin MURNI GBOLEH KATA LAENN!!
type StatusKawin = "Jomblo" | "Menikah Sejahtera";

type PasienRS = {
    nama: string;
    // BORGOL MENGANDELKAN TYPE ALLIAS DIATTAS!
    statusRanjang: StatusKawin; 
}

// Implementatnsio :
let pasien1: PasienRS = {
    nama: "Udin Sedung",
    statusRanjang: "Jomblo"   // ✔️ Berhasi AMN!
    // statussRanjang: "TdkDiketahui"   // ❌ ERROR! Kata "TdkDIkatahi" kaga kedafr dsalah statu pilhn Type ALias StatusKwn!!
}
```

Inhilah asalan kenapa Developer Frontend Modern bs ngerun Ratusan ribu baris kode Front End React tanpa Takut Crash ditengah Jalan krna Typo Mleset Key Objekc nya! Gila kan!

---
[⬅️ Sebelumnya: Fungsi Tpe Return](../05-Fungsi-Type/README.md) | [Lanjut ke Hak CIpta OOP Class Biasa ➡️](../07-Class-OOP-Strict/README.md) | [🏠 Daftar Isi](../README.md)
