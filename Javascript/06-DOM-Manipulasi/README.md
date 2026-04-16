# 06 - DOM Manipulation (Pondasi Web Hidup!)

DOM (*Document Object Model*) adalah "jembatan" bagi file JavaScript untuk bisa membaca isi file HTML kamu. Dengan ilmu DOM ini, Website kamu tidak hanya selembar poster diam, melainkan dapat di-klik dan berubah warna!

## 1. Menangkap Elemen HTML

Di file HTML anggap kita punya elemen judul dan tombol:
`<h1 id="judulKu"> Halo Website! </h1>`
`<button id="tombolKu"> Ganti Judul </button>`

Di dalam file JS, kita akan panggil dia menggunakan `document`:

```javascript
// Peringatan: Script ini umumnya dipasang menempel ke dalam HTML kamu

// Tangkap elemen h1 berdasar nama ID nya
const teksJudul = document.getElementById("judulKu");

// Tangkap tombol
const tombolSakti = document.getElementById("tombolKu");
```

## 2. Mengubah Isi (Teks / CSS Style)

Kalian sudah menangkap gawangnya, saatnya dijebol isi teks dan warnanya.

```javascript
// Ubah teks tanpa disentuh di HTML nya
teksJudul.innerText = "Wow, diubah oleh JS gais!";

// Kita kasih "Suhu CSS" ke elemen HTML-nya
teksJudul.style.color = "red";
teksJudul.style.fontSize = "50px";
```

## 3. Memberikan "Aksi / Event" Saat Diklik!

Mari kita buat tombolnya bekerja agar sewaktu diteksekusi dia melakukan suatu fungsi. Dalam JS hal tersebut memanggil metode rahasia bernama `addEventListener`.

```javascript
// Pasang alarm pada si Tombol, bahwa kalau di klik (click), lakukan perintah ini...
tombolSakti.addEventListener( "click" , () => {
    
    // Logic ketika diklik ada di sini
    alert("WEEEE, KAMU KLIK TOMBOL YA?!");

    // Atau ganti warna bodynya
    document.body.style.backgroundColor = "black";
    
});
```

Dan dengan bekal bab ini, **Selamat!** Kamu sudah menguasai arsitektur bagaimana sebuah web Interaktif dibangun tanpa bantuan Framework (alias Vanilla JS murni)!

---
[⬅️ Sebelumnya: Algoritma Dasar](../05-Algoritma-Dasar/README.md) | [Lanjut ke Materi Asynchronous ➡️](../07-Asynchronous/README.md) | [🏠 Daftar Isi](../README.md)
