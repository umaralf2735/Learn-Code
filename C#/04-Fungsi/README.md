# 04 - Method & Parameter

Di C#, fungsi disebut "Method". Metodenya juga punya deklarasi balikan dan tingkat Enkapsulasi (public/private).

```csharp
using System;

class Program {
    
    // Static agar bisa dipanggil sama fungsi static si Main. Return nya MWAJIB Integer!
    static int HitungGabung(int a, int b) {
        return a + b;
    }
    
    // Voide jika gakan ngasilin output balikan
    static void PrintNamaOase(string ns) {
        Console.WriteLine("Halo! " + ns);
    }
    
    static void Main() {
        int hasil = HitungGabung(20, 30);
        Console.WriteLine($"Hasil gabung: {hasil}");
        
        PrintNamaOase("Andi");
    }
}
```
---
[⬅️ Sebelumnya](../03-Array-dan-Koleksi/README.md) | [Lanjut ➡️](../05-Class-OOP/README.md) | [🏠 Daftar Isi](../README.md)
