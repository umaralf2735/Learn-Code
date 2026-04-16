# 07 - Pewarisan & Polimorfisme (Darah Daging)

Sama seperti materi JS Bab 9. Kenapa nulis Class yang nyaris kembar dua kali ulang? Pakai sistem Pewarisan (Inheritance).

## Turunan Asli pakai Titik Dua `:`

```csharp
using System;

// INDUK
class MahlukHidup {
    public void Napas() {
        Console.WriteLine("Hhhaaa (ngirup oksigen)");
    }
    
    // VIRTUAL: NGASIH IJIN KALO ANAKNYA MAU NGELANGGAR DAN BIKIN ATURAN SUARA KERAS SNDIRI!
    public virtual void Bersuara() {
        Console.WriteLine("Suara Ghoib");
    }
}

// ANAK TURUNAN (Ikut mewarisi napas)
class Manusia : MahlukHidup {
    public void Sekolah() {
        Console.WriteLine("Rajin skripsi gan!");
    }
    
    // OVERRIDE: Menindas kekuatan bapaknya!!
    public override void Bersuara() {
        Console.WriteLine("Pagi lurddd!");
    }
}

class Program {
    static void Main() {
        Manusia andi = new Manusia();
        
        andi.Napas();    // Tembus loh mewarisi Induknya !!
        andi.Sekolah(); 
        
        // Siapa hayoo yg kepanggil? Suara Induk ato Anak? ANAK DONG KAN DI OVERRIDE!
        andi.Bersuara(); // Pagi lurddd!
    }
}
```

Disadari tidak sadar, waktu kalian bikin Game Character, itu Induknya cuman 1 (Benda Bernyawa). Anaknya 1000 Class Enemy yang berbeda-beda!

---
[⬅️ Sebelumnya: Enkapsulasi](../06-Encapsulation-Property/README.md) | [Lanjut ke Interface ➡️](../08-Interface/README.md) | [🏠 Daftar Isi](../README.md)
