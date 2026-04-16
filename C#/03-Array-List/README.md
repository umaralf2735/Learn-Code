# 03 - Array Lawas & Modern (List<T>)

Seperti bahasa tingkat tinggi, C# membedakan Kumpolan Data menjadi penampung permanen kaku (Array) dan penampung karet bisa melar mengecil dinamis (List).

## 1. Array Standar `[]`

Ukuran Array C# itu KAKU. Ketika dibentuk slot pesen 3 biji, maka mau selamanya tak bisa ditambah jadi 4 atau apalagi di kurang di buang slot isinya. (Mirip C Murni!) Karena dia mem-booking ruang memori khusus statis.

```csharp
// Pesan loker ukuran 3! GABISA DITAMBAH JUMLAH SLOTNYA.
int[] skor = new int[3];
skor[0] = 50;
skor[1] = 90;
skor[2] = 100;

// Cara gampangnya bisa langsung dituang isinya tanpa sebut slot number
string[] namaPemain = {"Joni", "Gatot", "Tono"};
```

## 2. List Super Fleksibel (`List<T>`)

Kamu pengen nambah slot nambah kotak kayak `.push` `.append` di bahasa Python ato JS? C# menggunakan modul `List<>` buat nyiptain Array Sihir.

**Harus import dulu dari atas:** `using System.Collections.Generic;`

```csharp
// Membikin kotak daftar yg tipe spesifik String. 
// Awal awal kotaknya beneran kosong plong.
List<string> rakBuku = new List<string>();

// Bebas nambahin sampai ratusan masukin trosss :
rakBuku.Add("Kancil dan Buaya");
rakBuku.Add("Buku Sejarah");

// Gampang juga buat nyopot barang (Bisa ngenetilang persisi Teks isinya!)
rakBuku.Remove("Buku Sejarah"); // BUWANGG!!!

Console.WriteLine($"Sisa koleksiku : {rakBuku[0]}");
// Hasil -> Kancil dan Buaya
```

List inilah yang jadi andalan Developer se-Eropa / US selama merajut *game engine Unity* maupun *Backend Server C#*.

---
[⬅️ Sebelumnya: Struktur Kontrol](../02-Struktur-Kontrol/README.md) | [Lanjut ke Method ➡️](../04-Method/README.md) | [🏠 Daftar Isi](../README.md)
