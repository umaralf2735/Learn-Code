# 01 - Dasar-Dasar C# (Senjatanya Windows & Unity)

Selamat datang di C# (C-Sharp)! Ini adalah bahasa modern buatan Microsoft. Kalau lu mau bikin Game pakai **Unity 3D** atau bikin aplikasi Desktop/Web *ASP.NET*, ini bahasa mutlaknya!

Sifatnya super terstruktur mirip Java, tapi penulisannya lebih enak kaya JS modern.

## 1. Tulang Punggung Class Utama

Semuanya di C# **WAJIB** berada di dalam sebuah Class.

```csharp
using System; // Import library dasar!

// Namespace = Group Folder agar nama class tidak bentrok
namespace ProyekGue {
    
    class Program {
        
        // Gerbang utama yang langsung dipanggil PC!
        static void Main(string[] args) {
            
            // Mencetak suara
            Console.WriteLine("Halo C-Sharp, Pembangun Unity Game!");
        }
    }
}
```

## 2. Deklarasi Variabel Strict

Karena ini strongly-typed, sama seperti TypeScript!

```csharp
int peluruSisa = 30;
string namaPlayer = "Joko Tarub";
bool apakahMati = false;

// INTERPOLASI STRING MAUT MIRIP JAVASCRIPT! (Pakai $ di depan)
Console.WriteLine($"Player {namaPlayer} nembak sisa {peluruSisa} perak.");
```

Itulah pemanasan dasar C#! Kita lanjut ke alurnya!
---
[Lanjut ke Struktur Kontrol ➡️](../02-Struktur-Kontrol/README.md) | [🏠 Daftar Isi](../README.md)
