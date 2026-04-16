# 04 - Method (Pabrik Mini)

Fungsi di dalam C# lebih bermartabat dengan sebutan `Method`, karena semuanya pasti nempel tak terlepas dari Class pembungkusnya (Secara tak langsung OOP Mutlak).

## 1. Return Void & Type Mutlak

Garis besar rumusnya yaitu:  
`[Akses] [Tipe Return] NamaAksi (Param) { }`

```csharp
using System;

class Mobil {

    // 1. VOID (Hampa, Ga Menghasilkan balikan ke Variabel Pemetik, cmn beraksi)
    public void BunyiKlakson() {
        Console.WriteLine("Tin Tiin!!!");
    }

    // 2. MENDEMAND KEMBALIAN! Wajib Int lho ya!!
    public int KalkulasiIsiBensin(int liter, int bayar) {
        int harga = 10000 * liter;
        int kembalian = bayar - harga;
        
        return kembalian; // kalau direturn dengan nilai String, Error dongeng!!
    }

}
```

## 2. Parameter "Keyword" Berlabel

Di bahasa tua kalau salah ngasih urutan parameter itu kan fatal! Kalau nama param nya banyak, C# nyediain gaya ngetik dengan menyebutkan Namanya!!

```csharp
class Order {
    public void KirimBarang(string barang, string kotaKirim, bool pakeGoSend) {
        // ... logika..
    }
}

class Program {
    static void Main() {
        Order pesananKu = new Order();
        
        // Wah kacaw lupa urutannya klo polosan! 
        // pesananKu.KirimBarang(true, "Roti", "Jakarta"); // ERROR FATAL GA MASUK AKAL!
        
        // PAKE SEBUT NAMANYA LANGSUNG DI CODE !! (Tebakan bebas urutan!)
        pesananKu.KirimBarang( pakeGoSend: true, barang: "Roti Coklat", kotaKirim: "Jakarta" );
    }
}
```
Ini sangat memperindah code jika tim mu jumlah Developernya puluhan dan memelihara aplikasi raksasa.

---
[⬅️ Sebelumnya: Array Koleksi](../03-Array-List/README.md) | [Lanjut ke Hakikat Asli Class OOP ➡️](../05-OOP-Class-Object/README.md) | [🏠 Daftar Isi](../README.md)
