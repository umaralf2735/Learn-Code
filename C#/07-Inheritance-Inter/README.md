# 07 - Warisan (Inheritance) & Interface

C# juga menggunakan Tanda Titik Dua `:` layaknya C++ untuk menurunkan sifat ke anaknya.

```csharp
using System;

// BAPAK
class PemainBiasa {
    public void Berjalan() {
        Console.WriteLine("Step.. step..");
    }
}

// ANAK TURUNAN
class PemainSuper : PemainBiasa {
    public void Terbang() {
        Console.WriteLine("Swwwuuuush, aku di lagit!");
    }
}

class Program {
    static void Main() {
        PemainSuper ironMan = new PemainSuper();
        ironMan.Berjalan(); // WARISAN
        ironMan.Terbang();  // DIRINYA SENDIRI
    }
}
```

## Interface
Interface sangat krusial di C#. Dia digunakan sebagai "Perjanjian Kontrak Wajib".
Nama antarmuka C# biasanya diawali huruf **I**.
```csharp
interface ISeranganBakar {
    void BakarMusuh(); // Semua class yang makai kontrak ini WAJIB BIKIN ISI fungsi inii!
}
```
---
[⬅️ Sebelumnya](../06-Property-Lanjut/README.md) | [Lanjut ➡️](../08-LINQ/README.md) | [🏠 Daftar Isi](../README.md)
