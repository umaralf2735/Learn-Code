# 09 - Generics (Type Sebagai Parameter Gaib!) 

Materi `Generics` ini adalah Puncak ilmu ketatnya TS. Jika kalian dpt tes Intervirew Perushaaan ngliat kodingan pny tanda Kurung Lancip `<T>`.. brrta itu lg manggil ilmu ini!

## Memecahkan Masalah Kebuntuan Tipe
Ceritanya lu bikin Fungsi KARDU yang bisa nerima barang String apa Aja untuk nampung. Trs Tiba2 Boss lo mnta "Bro Bkinin fungsi itu juga donk buat NRIMA Angka!" Masa elo mo Kopi-Paste fungsi yg sma 2 kali dan cmn ganti ganti Tipe paramterny doag jd `: number` ?! Konyol!

**Ilmu Generics `<T>` Datang!! (Tipe Yang Dilembar Bebas Kaya Paramter Variable)**

```typescript
// -- BACA ATURAN MAINNYA--
// 1. Gua Punya Fungsi KardusKeren. Pny Lobang Type <TipeBebasAppn>. 
// 2. Isian parameter (BendaMasuk) bakal diborgol mnGIKUTI <TipeBebas> DiatASS!
// 3. RETRUN NYa JUGA MENBUGTITIKU <TipeBbasAppnn> diatas tsbb!

function masukkinKeKardusKeren<T>(bendaUjainnya: T): T {
    console.log("Aku bru naruh benda ni bro..");
    // Balikkin lagi kkuar stkh dproses
    return bendaUjainnya;
}


// SAAT PANGGILAN TERJADI!!!! KITA TANCAPIN KURUNG LANCIP MINTA TIPE APA!!!
// 1. Minta Bkinin yg Verrsi String!!
let hasilBuah = masukkinKeKardusKeren<string>("Pisang Goreng");

// 2. Minta Bikinin Verrsi Angka doang ahh!! 
let gajigan = masukkinKeKardusKeren<number>(9000000000);


// ❌ TS BAKAL NGAMUK KERAS KALO ELO SLH MASUNKON TIPE YG UDH DPILH:
// let mcamAn = masukkinKeKardusKeren<boolean>( "KATA TEXT" ); // ERROOOOOR!! Minta boolean di lobangan lancip tp u nymbngn STRING!!

```

Inlah Trik paling gila di React ngerujuk Redux dan Axios `axios.get<InterfaceTamuDB>('url')`. TibeTibe hsil kemnbalian Axiosnya LGSUNG Nngitil auto complkete denga properti `Tamu DB` murnii tnpa capek2 ngecek! The Magivc Of TS Generics. 

---
[⬅️ Sebelumnya: Emnummberable](../08-Enum/README.md) | [Lanjut ke Konfigurrasi JS Tscnfig ➡️](../10-Konfigurasi-TS/README.md) | [🏠 Daftar Isi](../README.md)
