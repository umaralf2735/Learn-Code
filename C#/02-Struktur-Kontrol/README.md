# 02 - Struktur Kontrol Klasik

Mengingat akar usul C# adalah klan bahasa C. Semuanya sama 100% identik dengan bapak moyangnya Java maupun C++. Terkurung Kurawal `{ }`.

## 1. Percabangan Bawaan

```csharp
int umur_klien = 21;

if (umur_klien >= 18) {
    Console.WriteLine("Minuman Dewasa Dibuka!");
} else if (umur_klien >= 15) {
    Console.WriteLine("Remaja boleh di luar aja.");
} else {
    Console.WriteLine("Bocil Hus Hus!");
}
```

## 2. Looping For dan Foreach

Bisa dengan For hitungan angka:
```csharp
for(int x = 1; x <= 5; x++) {
    Console.WriteLine("Iterasi mesin ke-" + x);
}
```

Atau cara cantik untuk ngeluarin isi Laci Array, yakni `foreach`!
```csharp
string[] senjataku = { "Pistol", "Pedang", "Pisau" };

foreach(string barang in senjataku) {
    Console.WriteLine("Dikeluarkan: " + barang);
}
```

Itu saja! Sangat natural bagi kalian yang lahir dari kodingan Universitas awal!

---
[⬅️ Sebelumnya: Dasar-Dasar](../01-Dasar-Dasar/README.md) | [Lanjut ke Array Koleksi ➡️](../03-Array-List/README.md) | [🏠 Daftar Isi](../README.md)
