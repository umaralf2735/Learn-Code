# 02 - Seleksi & Looping C#

Sangat identik dengan pola Javascript / TypeScript, menggunakan kurung kurawal.

## 1. IF Biasa

```csharp
using System;

class Program {
    static void Main() {
        int skor = 90;
        
        if (skor >= 80) {
            Console.WriteLine("Lolos Masuk UI!");
        } else {
            Console.WriteLine("Belajar lagi ya dek!");
        }
    }
}
```

## 2. Looping (Harta Karun `foreach`)

C# punya cara gampang memutar array layaknya JS `for..of` atau PHP `foreach`.

```csharp
using System;

class Program {
    static void Main() {
        string[] kota = {"Jakarta", "Bandung", "Bali"};
        
        // Bacanya: Untuk setiap k didalam list Kota
        foreach (string k in kota) {
            Console.WriteLine($"Jalan-jalan ke: {k}");
        }
    }
}
```
Pendekatang `foreach` ini nanti super sering dipakai di Unity memutar array Musuh.
---
[⬅️ Sebelumnya](../01-Dasar-Dasar/README.md) | [Lanjut ➡️](../03-Array-dan-Koleksi/README.md) | [🏠 Daftar Isi](../README.md)
