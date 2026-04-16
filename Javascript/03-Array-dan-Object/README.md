# 03 - Array dan Object

Cara menyimpan banyak data ke dalam memori komputer, supaya tidak perlu membuat ribuan variabel!

## 1. Array

Array di JavaScript sangat fleksibel, kalian bahkan bisa mencampur bermacam tipe data di array yang sama, lalu ukurannya dapat otomatis menyesuaikan (tanpa ada pemisahan antara Array tetap dan Slice seperti di Golang).

```javascript
// Membuat Array
let laciKu = ["Kunci", 1000, true, "Gembok"];

// Mengakses index pertama
console.log(laciKu[0]); // Output: Kunci

// Menambah data baru ke belakang laci
laciKu.push("Kertas");

// Menghapus data paling belakang
laciKu.pop();

console.log(laciKu); // Output: ["Kunci", 1000, true, "Gembok"]
```

## 2. Object

Object di JavaScript mirip dengan konsep *Struct* atau *Dictionary/Map* di bahasa lain. Kita pakai nama/label (Disebut Key/Properti) untuk menyimpan isi / kembaliannya (Value).

```javascript
// Mendefinisikan object Siswa menggunakan `{}` (Kurung kurawal)
let Siswa = {
    namaLengkap: "Rina Kumala",
    kelas: 11,
    jurusan: "IPA",
    sedangAktif: true
}

// Cara mengakses informasinya:
console.log("Nama Murid:", Siswa.namaLengkap); // Pakai titik (.properti)
console.log("Kelass:", Siswa["kelas"]);        // Pakai bracket
```

Kita dapat menggabungkan Object ke Dalam Sebuah Array:
```javascript
let daftarTeman = [
    { nama: "Ucup", domisili: "Bandung" },
    { nama: "Joni", domisili: "Jakarta" }
];

console.log(daftarTeman[0].nama); // Menampilkan "Ucup"
```

---
[⬅️ Sebelumnya: Struktur Kontrol](../02-Struktur-Kontrol/README.md) | [Lanjut ke Fungsi ➡️](../04-Fungsi/README.md) | [🏠 Daftar Isi](../README.md)
