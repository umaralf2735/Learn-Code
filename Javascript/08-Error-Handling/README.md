# 08 - Error Handling (Try...Catch)

Terkadang program kita berjalan mulus, tapi karena internet putus atau data yang dimasukkan kosong, mendadak kodenya "Crash". Untuk menghindari hal itu, ada ilmu Pertahanan yang disebut **Try and Catch**.

## Menjerat Kode Rawan

Bungkus program-program berbahaya kamu (seperti memproses file bacaan atau menembak ke server luar negeri) menggunakan `try`. 
Kalau nyangkut sesuatu, blok `catch` otomatis bakal ngejagain jatuhnya sehingga website kamu tidak akan rusak.

```javascript
// Bayangkan fungsi ini men-download data berukuran besar
function narikData() {
    let berhasilMurni = false;
    
    if(!berhasilMurni) {
        // melempar alarm error murni!
        throw new Error("Gagal Menarik! Internet Putus!");
    }
    return "Data Terdowload Bro!";
}


// INILAH PERTAHANANNYA
try {
    console.log("1. Program Mulai!");
    
    let barang = narikData(); // DISINI PROGRAM AKAN PATAH/TERLEMPAR KE BAWAH!
    
    console.log("Program selamat dari hambatan narikData:", barang); 
    
} catch (tangkapan) { // "tangkapan" adalah benda error yang dilempar dari dalam fungsi tadi.
    
    console.log("YAH ADA KENDALA:");
    console.log(tangkapan.message); // Output: Gagal Menarik! Internet Putus!
    
} finally {

    console.log("----");
    console.log("Aku selalu dieksekusi entah gagal atau enggak..");
}
```

---
[⬅️ Sebelumnya: Async/Await](../07-Asynchronous/README.md) | [Lanjut ke Class OOP ➡️](../09-Class-OOP/README.md) | [🏠 Daftar Isi](../README.md)
