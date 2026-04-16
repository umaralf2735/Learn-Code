# 08 - LINQ (Sihir Array C# The Best!)

Apa jadinya kalau Database SQL disatukan ke dalam List C#? Jawabannya adalah **LINQ**.
Kalian tidak perlu *Foreach loop* manual lagi buat nyari data genap/ganjil!

Ini fitur kebangaan Microsoft yang gak ada di Java murni!

```csharp
using System;
using System.Collections.Generic;
using System.Linq; // WAJIB DI IMPORT!!

class Program {
    static void Main() {
        List<int> duitJatuh = new List<int> { 500, 10, 850, 4, 1000, 20 };
        
        // --- NYARING UANG YANG DIATAS 100 DOANG ----
        // Pake Lambda / Arrow Function =>
        var duitGede = duitJatuh.Where(uang => uang > 100).ToList();
        
        // Panggil dan Cetak
        Console.WriteLine("Duit besar doang:");
        foreach(var d in duitGede) {
            Console.WriteLine(d); // Output: 500, 850, 1000
        }
        
        // NGURUTIN KECIL KE BESAR (Gausah susah2 Bubble Sort C kan!!)
        var sudahUrut = duitJatuh.OrderBy(x => x).ToList();
    }
}
```

Nanti kalau kerja bikin Web pakai ASP.NET, LINQ ini bakal otomatis disulap jadi Query Database sungguhan di belakang layar! Asik banget!
---
[⬅️ Sebelumnya](../07-Inheritance-Inter/README.md) | [Lanjut ➡️](../09-Delegate-Events/README.md) | [🏠 Daftar Isi](../README.md)
