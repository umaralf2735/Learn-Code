# 09 - Cetakan Pabrik Modern (Class OOP Javascript)

Di Bab 3 kalian udah belajar bikin data pakai *Object Mentah `{ }`*. Tapi gimana kalau kalian mau bikin *1000 Kucing* beda beda namanya? Masa ngulang nulis object literal `{ }` 1000 biji file. Kacau.

Sejak Tahun 2015, Javascript membikin fitur **Class Blueprint**. 
(Ini ilmu standar Java & C++, dipungut dan diadopsi ke Javascript modern agar kode perusahaan raksasa bisa dirapikan struktur hirarkinya).

## 1. Memahat Cetakan Utamanya

```javascript
// Nama cetakannya biasa pakeawalan huruf KAPITAL bos
class AnggotaSekte {
    // Method Sakral constructor! (Otomatis jalan PERTAMA KALI setiap Lo Cetak Umat Baru)
    constructor(nm, levelGali) {
        this.namaUmat = nm;               // This = miliknya anak yg baru tercetak ini
        this.pangkatLevel = levelGali;
        this.masihIdihup = true;
    }
    
    // Nempel method khusus yg cm bs dipuntain si anak Umat
    lakukanTapa() {
        console.log(`Ahhh... Pukulan naga, dari master ${this.namaUmat} level ke ${this.pangkatLevel}`);
    }
}
```

## 2. Melt & Mangkuk Cetakannya Mnjadi Objek Hidup!

Gunakan alat pemanas penuangan logam `new` diikuti pameanggilan cetakannya.

```javascript
// Bikin anak!
let anakPertama = new AnggotaSekte("Jaka Petir", 55);
let anakMuda = new AnggotaSekte("Siti Sakti", 1000);

// Mereka punya sifat mandiri tanpa nyenggol orang sebelahnya
anakPertama.lakukanTapa(); // ngeluarin Pukulan .. master Jaka Petir
anakMuda.lakukanTapa();    // ngluearin Pukulan master Siti.
```

## 3. Pewarisan Ilmu Genetik (`extends`)

Males ga tuh kalo di game, Musuh Biasa beda tipiiiis doang sama Boss, tp elo harus buat Blueprint dari 0 lgi bener bener panjang?
Bisa numpang Waris Gen dari bapaknya!!

```javascript
// Dia mewarisi 100% darah daging si AnggotaSekte!! (Gaperlu nulis lg dalemnya!!)
class MahaDewa extends AnggotaSekte {
    constructor(nm, levelGali, sayapLebar) {
        // SUPER() WAJIB ADA BUAT MANGGIL DARAH CONSTRUCTOR PUNYA INDUKNYA (lempar nam dan levl ke ats!)
        super(nm, levelGali); 
        this.panjangSayap = sayapLebar;
    }
    
    // Skill Eksklusif cuman ada d ras Dewa
    terbangKencang() {
        console.log("Whooosh... Kepak sayap " + this.panjangSayap + " m terbang lgsg menembus awann!");
    }
}

let zeusJS = new MahaDewa("Zeus Dewa Langit", 9999, 50);

// HEBAT!! BISA MAKE SKILL BAPAKNYA DAN SKILL SENDIRINYA!
zeusJS.lakukanTapa(); 
zeusJS.terbangKencang(); 
```

Selamat, kalian resmi menjadi *Software Engineer* Backend beraliran Object Oriented murni layaknya sepuh-sepuh Java di luar sana!

---
[⬅️ Sebelumnya: Tangkap Error](../08-Error-Handling/README.md) | [Lanjut ke NPM Package ➡️](../10-NPM-dan-Modul/README.md) | [🏠 Daftar Isi](../README.md)
