# 09 - Pemrograman Berorientasi Objek (Class)

Sebenarnya JS terlahir bukan bahasa yang menganut OOP semurni C++ atau Java. Dulu untuk membuat Class di JS itu rumit sekali. Namun untungnya di **(ES6)** dilahirkan sebuah sistem `class` terstruktur yang enak dibaca.

## Membuat Blueprint

Bentuknya sekarang nyaris 100% sama dengan Java.

```javascript
class Mahasiswa {
    // Dipanggil saat Class ditiupkan menjadi Objek hidup
    constructor(namaAwal, jurusan) {
        this.nama = namaAwal;
        this.jurusan = jurusan;
    }

    // Metode internal (Function di dalam struktur Class gaboleh pake kata function)
    belajarDong() {
        console.log(`${this.nama} anak ${this.jurusan} lagi serius baca modul!`);
    }
}

// Mari cetak blueprintnya:
let mhsOki = new Mahasiswa("Oki Setiawan", "Sistem Informasi");

mhsOki.belajarDong(); 
```

## Pewarisan (Inheritance) - Extend

Bayangkan mau membedakan Dosen Sama Mahasiswa. Ya dua-duanya tetep Manusia toh? Maka `class Manusia` bia diturunin sifatnya ke kelas bawahnya.

```javascript
// KELAS INDUK
class Manusia {
    constructor(nama) {
        this.nama = nama;
    }
    tidur() {
        console.log(this.nama + " sedang zzzzzz..");
    }
}

// KELAS ANAK (Mewarisi sifat manusia)
class Dosen extends Manusia {
    constructor(nama, gelar) {
        super(nama); // Manggil constructor manusia! Wajib!
        this.gelar = gelar;
    }

    ngajar() {
        console.log(`Pak ${this.nama}, ${this.gelar} lagi nerangkan.`);
    }
}

const pakDosen = new Dosen("Agus", "M.Kom");
pakDosen.tidur(); // Dia mewarisi kemampuan tidur padahal ga punya method tidur!
pakDosen.ngajar();
```

---
[⬅️ Sebelumnya: Error Handling](../08-Error-Handling/README.md) | [Lanjut ke Modul NPM ➡️](../10-NPM-dan-Modul/README.md) | [🏠 Daftar Isi](../README.md)
