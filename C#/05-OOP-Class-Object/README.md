# 05 - Class OOP Sejati

C# adalah penganut "Kasta Murni OOP". Kau tidak dapat membuat fungsi menggelinding di luar sendirian seperti PHP / JS. Semuanya Harus nempel ke Punggung Class!

## Mencetak Pabrik Kuenya (Blueprint)

```csharp
using System;

// 1. KITA GA NULIS PROGRAM DI SINI. INI SEBATAS CETAKAN (CLASS) DILUAR SANA.
class Siswa {
    public string Nama;
    public int RataRata;

    // Ini dipanggil otomatis sekali waktu cetakan diciptakan lewat NEW
    public Siswa(string namaAnak) {
        Console.WriteLine($"Kelahiran anak baru bernama {namaAnak}!!!");
        this.Nama = namaAnak;
    }
    
    // Method/Tindakan miliki anak ini saja
    public void Belajar() {
        this.RataRata += 10;
        Console.WriteLine($"{this.Nama} Pinteran dikit. IPK nambah {this.RataRata}!");
    }
}


class ProgramUtama {
    // 2. DISINILAH KITA MAENNYA! (DARI METHOD MAIN YAH)
    static void Main() {
        
        // Memakai sihir NEW untuk melelehkan cetakan class menjadi objek hidup 
        Siswa muridTeladan = new Siswa("Rizky");
        
        muridTeladan.Belajar(); // Tindakannya eksklusif milik Rizky
        
    }
}
```

Bagi sebagian orang ribet (karena harus muter-muter file). Tapi bagi arsitektur tim 30 orang Developer raksasa, OOP ini kunci nyawa proyek selamat dari kegagalan.

---
[⬅️ Sebelumnya: Method](../04-Method/README.md) | [Lanjut ke Properties (Senjata Gampang) ➡️](../06-Encapsulation-Property/README.md) | [🏠 Daftar Isi](../README.md)
