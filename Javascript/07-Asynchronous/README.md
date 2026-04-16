# 07 - Asynchronous (Sihir Menembus Waktu)

Ini adalah BAB TERPENTING DAN WAJIB di seluruh jagat raya pertahanan Backend/Frontend JS. Kalau ga ngerti Async Javascript, fix kalian ga bakal lulus ditrima tes Interview di perusahaan manapun. Hahaha.

## Ilustrasi Dunia Nyata
Normalnya, kodingan lurus kebawah (*Synchronous*). Bayangin kamu pesen Nasi Padang. **Kalo Synchronous**, kamu MESTI nunggu di depan kasir bengong melongo (nge-freeze), gabeloh buka HP atau mesen teajus, nunggu ampe tu nasi padang kelar dibungkus. Lama banget bangat buang waktu.

**DI JAVASCRIPT (*Asynchronous*)**: Kamu pesen Nasi Padang, Mas-mas Kasirnya ngasih kamu "Nomor Antrian Janji". Nah sambil nunggu dibungkusin, kamu bebas main HP, jalan jalan nyari minum, nolak nyamuk (Aplikasi gabakal ngFreeze!). NANTI KALA NASI PADANGNYA JADI, Mas kasirnya yg meneriaki Nomor Antrian kamu! Keren Kan!!

## 1. Promise (Surat Perjanjian Janji)

Paling gampang dan tradisional. Digunakan kalau *ngambil barang dari Server AWS*.

```javascript
// Bayangkan fetch ini adalah kamu minta data puluhan ribu KTP dari database pemerintah pusat. 
// Tentu lodingnya butuh waktu 3-5 detik donk internetnya?

console.log("1. Mesen Pesenan Ke Kasir..");

// Pake .then() untuk Nampilin kalo janjinya SETELAH (Then) Sukses!
fetch("https://jsonplaceholder.typicode.com/users")
    .then( response => response.json() ) // OTW Diubah jd object
    .then( hasilAsli => {
        console.log("3. YES PESANAN SIAP!!", hasilAsli[0].name); 
    })
    .catch( err => {
        // Pake .catch buat KALO ERROR KONEKSI LEMOT JANJI GAGAL
        console.log("Wah BAPAK KASIRNYA NIPU, SERVER DOWN", err);
    });

console.log("2. Sambil nunggu server ngejawab, aku tak nyapu lantai ah..");
```
> **Lihat urutan angkanya di log kalian?! Yang muncul duluan adalah angka `1`, LALU `2`, DAN SETELAH BEBERAPA DETIK BARULAH MUNCUL ANGKA `3`! Ga berurutan coy.** 

## 2. Jurus Dewa Masa Kini (`Async / Await`)

Karena pakai `then()` bersusun susun bikin kode keliatan jelek kayak tangga. Programmer NodeJS nyiptain keyword modifikasi gaib: `async` dan `await`. Minta PC berbohong supaya "seakan akan berurutan Synchronous mulus lagi penylisannya kaya bahasa PHP/Python"!

```javascript
// FUNGSI INI WAJIB DI BERIKAN MANTRA (async) DI DEPAN! 
const ambilDataRahasiaSekarang = async () => {
    try {
        console.log("Tunggu ya bosque tarik data dl...");
        
        // Kasih mantra AWAIT (Nungguin) di depan perintah yg ngasih Janji / Loding
        // KODE GA BISA LANJUT KE BAWAHNYA SBLM BARIS AWAIT BERES!
        const serverTarik = await fetch("https://jsonplaceholder.typicode.com/users");
        
        // Pake await lg krn nntrac json butuh mili-detik janji jg
        const objAsli = await serverTarik.json(); 
        
        console.log("ALHAMDULILAH BERES NIH BOSS SI :", objAsli[0].name);
        
    } catch(err) { // nangkap klo error
        console.log("Kiamat koneksi bos: ", err);
    }
}

ambilDataRahasiaSekarang();
```

Syntax `async/await` di atas adalah **jantung paling bernilai** di ekosistem Backend MongoDB Mongoose Nodejs kalian nantinya. Tanpa hal ini, database query tidak akan terjadi!

---
[⬅️ Sebelumnya: DOM](../06-DOM-Manipulasi/README.md) | [Lanjut ke Penanganan Error ➡️](../08-Error-Handling/README.md) | [🏠 Daftar Isi](../README.md)
