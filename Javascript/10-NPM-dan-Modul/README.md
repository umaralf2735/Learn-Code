# 10 - NPM dan Sistem Modul (ESM)

Kalau kamu sudah melesat masuk ke tahap membuat Website pakai React/Next.js, ini materi paling penting yang bakal diklik harian.

## 1. Import dan Export File Kamu

File js 1: `kalkulator.js`  
File js 2: `main.js`  
Gimana caranya file `main.js` narik kodingan dari `kalkulator.js` biar ditaruh rapi? Gunakan **ES Modules (import / export)**.

*Perintah di `kalkulator.js`:*
```javascript
export function tambah(a,b) { return a+b; }
export const PHI = 3.14;
```

*Perintah tarikan di file `main.js`:*
```javascript
// Narik 2 instrumen buatanmu sendiri
import { tambah, PHI } from './kalkulator.js';

console.log( tambah(2,4) ); 
```

*Syarat: ini gabisa dijalanin polosan murni HTML tua ya, harus dijalani via sistem server kekinian Node.js atau script tag module.*

## 2. Mengenal Node Package Manager (NPM)

Karena kamu pasti kadang ga pingin bikin ulang roda ban mobil waktu merakit mobil, *programmer* dunia menciptakan NPM. NPM itu semacam supermarket Modul JS gratis terluas di dunia (NodeJS).

**A. Instalasi project di terminal**:
```bash
npm init -y
```

**B. Belanja Library Pihak Ketiga (Contoh Download `axios` buat narik API)**
```bash
npm install axios
```
Tiba tiba saja folder gaib bernana `node_modules` tercipta berisikan file kodingan orang!

Lalu kamu tinggal narik pakai nama di foldermu `import axios from 'axios';` dan Poommm!!!! Website mu mendadak punya kekuatan tarikan API *overpowered* buatan komunitas dunia. Disinilah rahasia website-website *pro* dibuat secara kilat!

---
[⬅️ Sebelumnya: OOP Class](../09-Class-OOP/README.md) | [🏠 Daftar Isi Utama](../README.md)
