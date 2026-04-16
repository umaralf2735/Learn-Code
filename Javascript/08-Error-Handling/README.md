# 08 - Penahan Hantaman Kesalahan (`Try ... Catch`)

Ingat, kodingan itu gampang sekali rusak. Gimana kalau di program Game yang kamu bikin, internet pemainnya tiba tiba putus? Atau user masukin "Teks Panjang" di isian yang harusnya minta "Nomor HP Umur"?

Aplikasi kalian bakal meledak dan menutup seketika dengan pesan Merah Mengerikan di layar! 

## Sang Kurungan Besi Anti Meledak!

Solusinya, kurung semua logika bahaya pemicu bom ke dalam blok `try`. Lalu sediakan keranjang penyelamat di bawahnya (`catch`). Kalau beneran meledak, ledakannya GA BIKIN MATI APLIKASI, tapi cuman masuk ke keranjang penyelamet secara mulus.

```javascript
console.log("-- Sistem Persenjataan Aktif -- ");

// BUNGKUS pakai kurungan sakti
try {
   // Coba deh kita pura pura panggil Variable Misteri yang belom dibikin dmnpun...
   console.log("Siapa namamu?", sangMahklukLuarAngkasa);
   
   console.log("Baris ini gabakal sempet kejalanin karena ledakan udah terjadi dluan di var misteri atas..");

} catch (errorObj) {
    // 🚨 KALO DI DALAM KURUNG TRY ADA ERROR APAPUN...
    // PROGRAM GA NGE-FREEZE/BERHENTI! TAPI LANGSUNG LOMPAT MANIS DI EKSEKUSI DI BARIS INI:
    console.error("WADUH KOMANDAN ADA GALAT: Laporannya: " + errorObj.message);
} finally {
    // 🛡️ Blok Finally itu pilihan, mau mati error atau lancar sukses, Blok FINALLY PASTI JALAN trhir (Biasa buat beres beres memori).
    console.log("-- Sistem pembersihan matikan radar radar aktif!! --");
}

console.log("Programku masih idup lho dan selamat sampe ekseksui sisa kode dibwh!");

```

## Kapan Seringnya dipakai?

1. Nyolok **Database MongoDB/Postgres** (Takut salah username / password salah).
2. Mangil **REST API Luar** dengan *(Async/Await)* seperti yg kalian udah cicipi di Bab 7 seblumnya!
3. Ngebaca memori File sistem Komputer yang ternyata foldernya belum ada dibagung (*File I/O*).

Amankan semua sisi liar kodemu pakai kurungan maut ini!

---
[⬅️ Sebelumnya: Async Menembus Waktu](../07-Asynchronous/README.md) | [Lanjut ke Class Blueprint ➡️](../09-Class-OOP/README.md) | [🏠 Daftar Isi](../README.md)
