# 08 - Interface (Kavling Aturan Mutlak)

Sama seperti materi `Interface` punya TypeScript! Interface itu BUKAN CLASS.

Interface adalah surat kontrak wajib yang memaksa orang lain (Siapapun Class nya) harus dan wajib punya metode A dan tipe B kalaau nekat meneken jalinan kerja sama ini.

Biasanya nama Interface selalu diawali halusnya oleh Huruf I kapital (`IHewan`, `ILabel`, dll).

## Tanda Tangan Kontrak

```csharp
using System;

// 1. SURAT KONTRAK (GABOLEH DIJALANIN MURNI)
interface IHewanBersayap {
    int JumlahSayap { get; set; }
    void MengepakkanGelombang();
}

// 2. KELAS YANG NGE TAKEN KONTRAKNYA (Kalo dia ingkar janji, merah amyar!)
class BurungMerpati : IHewanBersayap 
{
    // Coba aja sebaris ini dihapu, pasti Compile Error bilang = "Burung belum menyetor metode kepak dari janji interface!"
    public int JumlahSayap { get; set; }

    public BurungMerpati() {
        JumlahSayap = 2;
    }

    // Melunasi janji Metode dari Kontrak
    public void MengepakkanGelombang() {
        Console.WriteLine($"Merpati goyang sayap nya yg {JumlahSayap} itu wush..");
    }
}


class Program {
    static void Main() {
        BurungMerpati piaraan = new BurungMerpati();
        piaraan.MengepakkanGelombang();
    }
}
```

Inilah cikal bakal semua plugin terstruktur, kamu maksa dev luar buat ikut nama fungsimu!

---
[⬅️ Sebelumnya: Inheritance](../07-Inheritance-Polymorphism/README.md) | [Lanjut ke LINQ Sakti ➡️](../09-LINQ-Collection/README.md) | [🏠 Daftar Isi](../README.md)
