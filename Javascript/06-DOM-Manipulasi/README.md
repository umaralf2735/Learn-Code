# 06 - Manipulasi DOM (Menyihir HTML yang Mati)

Selamat datang di ranahnya Dewa Frontend Javascript! Tanpa bab ini, programmu cuman nongol hitam putih di Console rahasia Developer F12 doang. DOM (*Document Object Model*) adalah jembatan sakti yang menghubungkan otak Javascript mu dengan Tag HTML di layar untuk dimanipulasi!

## 1. Menangkap Unsur Elemen (Kamera Pengintai)

Anggaplah kalian punya HTML kaya gini:
```html
<h1 id="judulBesar">Kantin Wakwaw</h1>
<p class="deskripsi">Selamat makan siang.</p>
<button id="tombolGanti">Klik Saya!</button>
```

Di JS, kita gunakan Radar Dewa: `document`.

```javascript
// Nangkap elemen pake ID (Yang Unik Cuman Satu Doang)
const judulElement = document.getElementById("judulBesar");

// Atau pake Query Selector (Super fleksibel kaya CSS Selektor biasa)
const pElemen = document.querySelector(".deskripsi"); 
```

## 2. Mengobrak Abrik Jeroan HTML di Layar

Setelah elemen ketangkep di JS. Kalian bisa tembak dia dengan titik dan ganti isi tekstur atau Warnanya!

```javascript
// Wah layarnya mendadak berubah text secara ghaib pas dijalanin nih Code!
judulElement.innerText = "Kantin Sukses Maju Mundur!!";

// Nyuruh tulisan paragraf warnanya jadi merah tomat dan Gede
pElemen.style.color = "tomato";
pElemen.style.fontSize = "30px";
```

## 3. Memberikan Telinga Pendengar (Event Listeners)

Ini dia esensi web modern Tiktok/IG/dsb. Bagaimana kalau diklik dia ngeluarin popup bunyi ledakan? Pasanglah `addEventListener`.

```javascript
const tombolMagic = document.getElementById("tombolGanti");

// Cara Baca: Hai tombol, pasang dong radar 'click', kalau denger lu kecentok klik, jalankan Arrow Fungsi ini!
tombolMagic.addEventListener("click", () => {
    // Apapun didalam kurung ini akan dijalanin SETIAP KALI user klik div buttonnya!
    alert("ADUH JANGAN DITEKAN KERAS KERAS BOS!");
    
    // Oh aku mau ganti judul web nya seketika!
    judulElement.innerText = "Waduh Tombolnya ditekan orang!!";
});
```

*Boom!!* Kalian resmi menjadi pembangun Web Frontend Interaktif!! Segala Library React / Angular dsb didirikan berangkat dari pondasi klik dan render milik DOM Manipulation di atas.

---
[⬅️ Sebelumnya: Algoritma Lanjut](../05-Algoritma-Dasar/README.md) | [Lanjut ke Asynchronous Sakti ➡️](../07-Asynchronous/README.md) | [🏠 Daftar Isi](../README.md)
