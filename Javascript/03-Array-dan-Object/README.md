# 03 - Array dan Object (Menyimpan Data Sekardus)

Kalau variabel di Bab 1 itu ember kecil. Gimanana caranya kalian nyimpan data nama-nama warga kecamatan yang isinya 1000 Jiwa? Masa harus *let warga1="Budi"; let warga2="Susi"* sampai ngetik seribu baris? 
Kenalkan **Array** (Kardus bergaris) dan **Object** (Peti Harta Karun).

## 1. Array `[]` (Si Lemari Bersusun Ber-Nomor)

Bayangkan sebuah loker besi berderet memanjang ke kanan. Tiap loker punya penanda urutan (Index) yang - anehnya komputer - SELALU DIMULAI DARI ANGKA NOL `0`! Bukan angka 1.

```javascript
// Bikin Array Laci
let laciOnderdil = ["Busi", "Rantai", "Kampas Rem", "Lampu"];

// Membaca Laci ke-Dua (Inget Mulai dari 0, berarti 'Rantai' itu index ke 1)
console.log( laciOnderdil[1] ); // Output: Rantai

// --- ALAT SULAP ARRAY JS ---

// 1. PUSH (Dorong Nambah Barang ke Ujung Laci Terakhir)
laciOnderdil.push("Oli Mesin"); 

// 2. UNSHIFT (Menyelak Menyodok Nambahin dipaling Kiri Depan Awal Banget!)
laciOnderdil.unshift("Spion"); 

// 3. POP (Membuang dan Ambil Barang paling Ujung Kanan)
laciOnderdil.pop(); 

console.log( laciOnderdil );
// Bentukannya jadi: [ 'Spion', 'Busi', 'Rantai', 'Kampas Rem', 'Lampu' ]
```

## 2. Object `{}` (Buku Catatan yang Punya Kunci / Nama Properti)

Array itu gak asik kalau datanya nyangkut ke Identitas. Misal `["Udin", 16, "Cilacap"]`, elu gabakal tau angka 16 itu umur atau ukuran celananya si Udin?
Maka Object hadir! Kita namain isian itu pake `Key : Value`.

```javascript
let profilHeker = {
    // Kunci Label : Isisannya Tipe Bebas
    namaAlias: "Mrd0c",
    umur: 22,
    skill: ["Ngeping Website", "Buka Port Jendela", "Bongkar FB Mantan"],
    sudahTobat: false
};

// Cara Akses nya gampang, cukup tembak nma variabel pakai TITIK '.'
console.log("Buronan heker kita bernama " + profilHeker.namaAlias);

// Narik Data Array dari dalem Perut si Object? Tembus tembusin aja Titik trs Siku!
console.log("Skill maut terfavorit: " + profilHeker.skill[2]); // Memanggil array indeks ke-2
```

## 3. Kombo Maut: *Array of Objects* (Format WAJIB REST API Backend Dunia)
Nanti waktu kamu narik data di Tokopedia atau Tiktok dr server database, formatnya PASTI begini: 

```javascript
let etalaseGundam = [
    { id: 1, nama: "Gundam RX-78", harga: 1500000 },
    { id: 2, nama: "Zaku Merah", harga: 500000 },
    { id: 3, nama: "Gundam WingZero", harga: 2000000 }
];

// Ngeluarin Harga Zaku Merah:
console.log("Harga Zaku: Milyaran Rp." + etalaseGundam[1].harga);
```

Bagi Backend Engineer JS, bab ini bagaikan bernapas dan makan nasinya sehari-hari.

---
[⬅️ Sebelumnya: Struktur Kontrol](../02-Struktur-Kontrol/README.md) | [Lanjut ke Fungsi ➡️](../04-Fungsi/README.md) | [🏠 Daftar Isi](../README.md)
