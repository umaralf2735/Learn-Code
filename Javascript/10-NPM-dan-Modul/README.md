# 10 - Menyedot Ilmu Maling Package Alam Semesta (NPM)

Di materi akhir pertapaan JS ini, pertanyaannya adalah: "Gimana caranya abang abang pro bisa bikin fitur kirim Email, Bikin Excel PDF, bikin AI, itu kode mentahnya dpt DRMNA?". Moso nulis dewe ngitu sejuta baris dari nol!?

Tentu Tidak! **Don't Reinvent the Wheel.** Programer sedunia membikin sekte bernama NPM (*Node Package Manager*). 

## 1. Belanja Senjata Library

Jika kalian punya Node.js terinstall. Kalian punya *Terminal maut CMD Node*.
Cukup inisiasi awalan sekaliumur hidup proyek ini buat ngelahirin buku akte kelahiran proyek (`package.json`), yaitu *`npm init -y`*.

Lalu download ilmu yg kalian idam-idamkan (Misalnya Ilmu Maut Baca Manipulasi Waktu: MOMENT):
`npm install moment`

Seketika file ghaib folder bernama `node_modules` meletus masuk ke directory kamu ngebawain milyaran file! (Ini folder keramat ga boleh diotak atik isi manualnya!).

## 2. Ekspor dan Import Modul Biasa Lintas File Lokal

**FILE 1: (mathSakti.js)** -> Si Tukang Bikin Senjata
```javascript
// Bikin benda
const kaliDua = (x) => x * 2;
const nilaiPI = 3.1415;

// DIUJUNG FILE WAJIB DI RELAKAN (DIBUKA PINTUNYA / DI EXPORT!!)
// Biar bs dipanggil module file sblah!
export { kaliDua, nilaiPI };
```

**FILE 2: (app.js)** -> Si Main File Pusat Pemenanggil
```javascript
// NARIK SEPERLUNYA AJA DARI KULKAS SEBELAH PAKE IMPORT ! Mantaapppp!!
import { kaliDua, nilaiPI } from './mathSakti.js';

console.log("Ngeliat nilai phi brap sih? Oh = ", nilaiPI);
console.log("Klo 5 dkali dua= ", kaliDua(5));
```

## 3. Import Sihir Dari NPM

Klo import library luar ga usah make embel-embel Path Relatif slash-titik `./` segala macem loh. Panggil namanya doang dari dewa NPM.

```javascript
// Narik lbrary besar yg di install npm td
import moment from 'moment';

// Boom, aku punya kekuatan manipulasi hitungan tanggal setara Facebook sekarang.
let sekarang = moment().format('MMMM Do YYYY, h:mm:ss a');
console.log("Waktu lokal saat ini: " + sekarang);
```

Dengan menguasai ekosistem NPM dan kemandirian arsitektur *Modules*.. Kalian resmi lulus bersertifikasi jalanan untuk melangkah membuat *React.js (Frontend)* ataupun *Express.js (Pembuat REST API Backend)* yang luar biasa!

---
[⬅️ Sebelumnya: Class Blueprints Cetakan](../09-Class-OOP/README.md) | [🏠 Daftar Isi Utama](../README.md)
