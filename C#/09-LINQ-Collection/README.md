# 09 - Keajaiban LINQ (Menembus List)

C# memang tak ada method kaya `.map()` `.find()` kaya di JS / Ruby. Tapi jangan cemas!

Bapaknya Windows menganugerahkan 1 sihir bernama **LINQ (Language Integrated Query)**!
Kamu ngerombak tumpukan Array / database SQL langsung di dalam bahasanya, pakek kata-kata Select dari SQL haha!

Harus menempel `using System.Linq;` dulu di plafon!!

## Sihir Menyedot Array 1 Baris

```csharp
using System;
using System.Collections.Generic;
using System.Linq; // JANGAN SAMPAI LUPA MANTRA DEWA NYA

class Program {
    static void Main() {
        List<int> daftarPoinku = new List<int> { 50, 90, 85, 20, 100, 77 };

        // 1. TUGAS: Cari KKM yang Lulus Aja! (Pakai WHERE - Persis kek JS Find/Filter!)
        // Bahasa Dewa (Arrow Lambda): carikan "x" yang mana "x lebih dr 75"
        var muridCerdas = daftarPoinku.Where(x => x > 75).ToList();

        Console.WriteLine("Yang Berhasil Masuk:");
        foreach(var c in muridCerdas) {
            Console.WriteLine(c); 
            // 90, 85, 100, 77
        }

        // 2. TUGAS: UBAH SEMUA NILAI JADI TEKS PASSPORT (Pakai SELECT kek MAP)
        var stempelData = daftarPoinku.Select(y => $"Siswa poin {y} Acc!").ToList();
        
        Console.WriteLine(stempelData[0]); // Siswa poin 50 Acc!
        
        // 3. TUGAS SUPER: Urutin Angkanya Dari yang Tergedeeeeeeeee!
        var urutanMulia = daftarPoinku.OrderByDescending(z => z).ToList();
        
        Console.WriteLine(urutanMulia[0]); // 100 Sang raja
    }
}
```

Disadari tanpa sadar, cara pakai dan fungsinya SAMA PERSIS dengan apa yang kita lakukan di modul Golang dan JS Algoritma Built In sebelumnya kan?

---
[⬅️ Sebelumnya: Interface](../08-Interface/README.md) | [Lanjut ke Try Catch ➡️](../10-Error-Exception/README.md) | [🏠 Daftar Isi](../README.md)
