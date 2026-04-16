# 08 - Enumerable (Si `enum` Penyelamat Magic Number)

Pernah kalian buka database atau file, teris ada angka: Pangkat Akun = `1`? Trs kalian bingung "Gila mna gw tau angka 1 itu User apa Admin yak?? Ini kode prbualn taun brpa nih gda dkumntsinyya". Yaps itu penaykit namnya *Magic Numbers*. 

TypeScript memperkennalkan **`enum`**. Tujuannya cumn 1 biar kodingan lu itu BISA DIBACA MANUSIA secara natural, bukan baca angka kaku.

## 1. Numeric Enum (Pembungkus Angka Urut)

Saat Lo Manggil Namnya, Yg kesimpen di PC nya sbnerna itu angknya!

```typescript
// NGUMPULIN JABATAN PAKE ENUM
// Biasakan nmnging dpannya huruf Gede!!
enum KastaKerajaan {
    RajaBebas = 1,     // Mulai dri nngka 1 ya bos jgn 0 ntar ak brabe pas ngceceknya d db ahaha
    Patih = 2,
    PrajuritRakyat = 3
}

// LIAT INI!! LU GAPERLU NULIS ANGKA 2 LG KLO MAU NGSET AKUN MNJDI PARJURIT!
// CUMAN NULIS PANGGIL ENUMNya dan NMBK .TITIK NYA AUTA NGLIUARIK OPOPSI NYA DI VSCODE LU!! 
let akunPakBowo: KastaKerajaan = KastaKerajaan.PrajuritRakyat;

// Buktiin isisinya angka ap Tkes?
console.log(akunPakBowo) // HASIL PRINT : 3 !!! BNER KANN!! Sbnrnya dy angak 3 di dlm hti mesinnn. Tpi mta manuskiamm bcny Teks Patih Prajurit!
```

## 2. String Enum (Lebih disukai Frontend Dev)

Kadang kita nyimpen dtbabes bkn bntuj angka int. Mlainakn String sperti "ADMIN". Enmum ttep kepke bgini!!

```typescript
// Klo yg ini ga bkal ngassilin nagka. Dia bkal ngassilin text stringn disblhny persis.
enum WarnaTombolErrorApp {
   SUCCESS_MANTAP = "HijauDaun",
   NGELAG_WARNING = "KuningNyala",
   BAHAYA_MATI    = "MerahDarah" 
}

// Bikin varabel dan lngusng bngkuz pke cetkana typnnya WarnaTomol ya!
let popupKuSkgTipeKmrn: WarnaTombolErrorApp = WarnaTombolErrorApp.SUCCESS_MANTAP;

console.log(popupKuSkgTipeKmrn); // Output jdnya TEKS: "HijauDaun"
```

Inilah rahasia Developer Perusahan sekelas Google ga pernagh bingung baca kode TS org lain mskipun udah lawas umurmnya karena smua plihan sdh di ENUM kan menajdi kata2 manusi awam yyang mudah ditebak.

---
[⬅️ Sebelumnya: CLASS OBJECK ORIENTED](../07-Class-OOP-Strict/README.md) | [Lanjut ke Tipe Parameter (Generics) Dewa ➡️](../09-Generics/README.md) | [🏠 Daftar Isi](../README.md)
