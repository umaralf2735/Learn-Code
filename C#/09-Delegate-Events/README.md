# 09 - Event & Delegate (Sensor Pengamat C#)

Gimana cara bikin tombol yang kalau diklik, dia ngirim pesan ke 4 sistem berbeda?
Jawabannya pakai sistem langganan Radio: **Events dan Action Delegate!**

Ini dipakai tiap hari di pembuatan karakter Action RPG (Misal: Kalau darah abis -> Trigger animasi mati -> Trigger suara mati).

```csharp
using System;

class BosIstana {
    // Bikin Radio Pemancar Pengumuman
    public event Action OnBosMati;
    
    public void DiPukul(int dmg) {
        Console.WriteLine($"Aghh aku kena pukol {dmg} dmg!");
        // Jika mati, Siararkan event!
        if(OnBosMati != null) {
            OnBosMati.Invoke(); // SIARKAN KE SEMUA YANG LANGGANAN!
        }
    }
}

class Program {
    
    // Ini si pendengar 
    static void BunyikanMusikKemenangan() {
        Console.WriteLine("Teeet Toreeeeet, Musik Kemenangan Menggema!!");
    }

    static void Main() {
        BosIstana gajah = new BosIstana();
        
        // TEMPELKAN PENDENGAR KE RADIO BOS (Pake tanda +=) ! 
        gajah.OnBosMati += BunyikanMusikKemenangan;
        
        // Aksi Game berjalan
        gajah.DiPukul(9999);
    }
}
```

Mantaappp!! Sistem Event C# memisahkan kode kita dengan sangat bersih.
---
[⬅️ Sebelumnya](../08-LINQ/README.md) | [Lanjut ➡️](../10-Async-Task/README.md) | [🏠 Daftar Isi](../README.md)
