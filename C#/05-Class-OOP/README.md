# 05 - Class & Object Mutlak

Unity Engine dipenuhi ratusan Class script, inilah jantung utama C#.

```csharp
using System;

class KarakterKsatria {
    public string namaHero;
    public int attackDmg;
    
    // Constructor (Dipanggil otomatis pake new)
    public KarakterKsatria(string n, int a) {
        namaHero = n;
        attackDmg = a;
    }
    
    public void Serang() {
        Console.WriteLine($"{namaHero} menebas kena {attackDmg} dmg!");
    }
}


class Program {
    static void Main() {
        // Cetak Class ke dunia PC!
        KarakterKsatria arthur = new KarakterKsatria("Hero King Arthur", 900);
        
        arthur.Serang();
    }
}
```
---
[⬅️ Sebelumnya](../04-Fungsi/README.md) | [Lanjut ➡️](../06-Property-Lanjut/README.md) | [🏠 Daftar Isi](../README.md)
