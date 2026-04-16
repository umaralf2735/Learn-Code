# 01 - Dasar-Dasar C#

C# sama seperti C++ dan Java, program utama selalu numpang hidup mutlak berada di dalam kotak besar bernama *Namespace* -> *Class* -> *Metode `Main`*.

## 1. Halo Dunia!

Kalau kalian pakai C# model jadul (sebelum .NET 6), bentuk template perawan nya gini nih (lumayan rumit karena sangat rapi struktural):

```csharp
using System; // Library pondasi utama

namespace PelajaranSatu // Folder wadah globalnya
{
    class Program // Badan program (Wajib huruf Gede awal)
    {
        // Fungsi pintu masuk dari segalanya
        static void Main(string[] args)
        {
            Console.WriteLine("Halo Kawan, C# Murni Hadir!");
            
            // Console.ReadLine() = Nahan Layar hitam Terminal biar ga ketutup instan sblm di-Enter
            Console.ReadLine(); 
        }
    }
}
```
*Catatan:* Kalau pakai .NET 6 ke atas, kodingannya bisa dihapus semuanyanya sisa 1 baris `Console.WriteLine("Halo");` doang (mirip Python/Nodejs!). Tapi aslinya tetep dibungkus invisible!

## 2. Tipe Data Kokoh

100% C# menolak kemalasan javascript. Mau ngetik tipe data? Harus teliti jenisnya.

```csharp
int duit = 50000;
double desimal_teliti = 3.14159;  // Double lebih panjang memorinya drpd Float
float  desimal_cepat = 5.5f;      // Kudu dilabelin f belakangnya biar nyadar
char satu_huruf = 'Z';
string nama = "Udin Coder";
bool jago_gak = true;

// Nempel ke teks output secara modern (String Interpolation = pakai $)
Console.WriteLine($"Nama saya {nama} saldonya sisa Rp.{duit} !");
```

---
[Lanjut ke Struktur Kontrol ➡️](../02-Struktur-Kontrol/README.md) | [🏠 Daftar Isi](../README.md)
