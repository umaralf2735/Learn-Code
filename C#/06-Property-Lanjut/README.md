# 06 - Properties (Get & Set Sakti)

Kalo di Java atau C++, lo harus bikin method panjang `public function getDarah()` dan `setDarah()` untuk menyembunyikan Private Data.
Sangat capek! 

Di C#, cukup pakai yang namanya **Properties (Get; Set;)**

```csharp
using System;

class Monster {
    // VARIABEL ASLI (DISIMPAN DI PRIVATE)
    private int _nyawaAsli;
    
    // PROPERTIES SAKTI (PUBLIC)
    public int NyawaGame {
        get { 
            return _nyawaAsli; 
        }
        set { 
            // 'value' adalah kata sakti bawaan C# untuk nilai yg dimasukkan user
            if(value < 0) {
                _nyawaAsli = 0; // Gak bisa minus!
            } else {
                _nyawaAsli = value;
            }
        }
    }
}

class Program {
    static void Main() {
        Monster bos = new Monster();
        
        bos.NyawaGame = -500; // DIcegat Set! Bakal jadi 0.
        
        Console.WriteLine($"Nyawa bos: {bos.NyawaGame}"); // Cetak 0 lewat Get!
    }
}
```

Bahkan bisa diringkas lagi cukup: `public int Level { get; set; }` doang! Ini yang bikin dev Game Unity betah koding C#.
---
[⬅️ Sebelumnya](../05-Class-OOP/README.md) | [Lanjut ➡️](../07-Inheritance-Inter/README.md) | [🏠 Daftar Isi](../README.md)
