# 07 - Asynchronous (Async/Await dan Promise)

Dalam JavaScript versi Modern, fitur terkuatnya adalah *Asynchronous* (Sama persis kayak Goroutine dari Golang yang sudah kita pelajari).

Dalam pemrograman Javascript konvensional, ketika program lagi disuruh Download Video atau nunggu data API server, halaman Website otomatis bakal Nge-Freeze (ngelag patah-patah). Fitur **Async/Await** menyelamatkan hari tersebut!

## 1. Apa itu Promise (Janji)?

Daripada menyuruh JS macet disatu perintah untuk menunggu hasil, kita buat fungsi untuk merilis tiket bernama **"Promise" / Janji**. Maksudnya: "JS, tolong kamu kerja ini di latar belakang, nanti kalau udah selesai atau ditolak, kabarin ya!".

```javascript
let kerjaBeresinTugas = new Promise( (suksesDitepati, gagalDiingkari) => {
    let semuaSelesai = true; // Anggaplah udah kelar kerjanya

    if (semuaSelesai) {
        suksesDitepati("Mantap Bang, Tugas selesaii!");
    } else {
        gagalDiingkari("Maaf ya bang.. males");
    }
});

// Menagih Janji pakai ".then()" kalau sukses, dan ".catch()" kalau gagal :
kerjaBeresinTugas
    .then( (kabarSukses) => console.log(kabarSukses) )
    .catch( (kabarGagal) => console.log(kabarGagal) );
```

## 2. Cara Termudah: Pakai Modern Async/Await (🌟 Bintang Utama JS)

Ribet pakai `.then()` dan `.catch()`, apalagi kalau fungsinya turun-menurun. Maka diciptakan format baru agar kita bisa menulis kode nunggu *background di server* seolah-olah program biasa!

Cukup taruh `async` diperintah function utamanya, dan ketik kata paksaan menahan waktu menggunakan `await` di baris yang membutuhkan waktu agak lama.

```javascript
// Bayangin ini fungsi dari Server Google (butuh waktu 2 detik)
function tarikDataUser() {
    return new Promise(selesai => {
        setTimeout(() => selesai({ nama: "Budi", status: "Admin" }), 2000); // Tahan nafas 2 detik
    });
}

// Tambahkan "async" di fungsinya biar dapat power
async function tampilkanData() {
    console.log("Sedang menarik data... mohon tunggu");

    // Paksa browser menunggu fungsi yg lambat dibawah kelar. Selama menunggu, JS akan kerja lain.
    let datanya = await tarikDataUser(); 

    console.log("Data selesai turun!");
    console.log(`Halo bos admin ${datanya.nama}!`);
}

// Panggil!
tampilkanData();
```

Format *Async / Await* inilah yang nantinya paling sakral kamu gunakan manakala bekerja menggunakan Framekwork (React/Vue/Next/AdonisJS).

---
[⬅️ Sebelumnya: DOM Manipulasi](../06-DOM-Manipulasi/README.md) | [🏠 Daftar Isi Utama](../README.md)
