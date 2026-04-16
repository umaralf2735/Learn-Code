# 03 - List (The Modern C# Array)

Di C# murni, Array tradisional `string[]` itu SANGAT kaku dan ngga bisa nambah slot baru (Mirip Bahasa C).
Nah maka dari itu Microsoft ngasih sihir bernama **`List<T>`**! Ini mirip banget sama Vector di C++ atau Array di Javascript.

```csharp
using System;
using System.Collections.Generic; // Wajib import List Collections!

class Program {
    static void Main() {
        
        // DECLARASI LIST (Dinamis)!
        List<string> ranselBarang = new List<string>();
        
        // PUSH item dari depan! (Di C# namanya Add)
        ranselBarang.Add("Pistol");
        ranselBarang.Add("Medkit");
        
        // Ngakses jumlah isi:
        Console.WriteLine($"Isi tasku ada {ranselBarang.Count} buah!");
        
        // Ngambil datanya:
        Console.WriteLine($"Senjata gw: {ranselBarang[0]}");
    }
}
```
---
[⬅️ Sebelumnya](../02-Struktur-Kontrol/README.md) | [Lanjut ➡️](../04-Fungsi/README.md) | [🏠 Daftar Isi](../README.md)
