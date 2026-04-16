# 10 - Penjinak Bom Error (.NET Exception)

Pernah ngalamin aplikasi di warnet mendadak nge *crash* terus ada tulisan peringatan silang putih merah ngongol dari pop-up windows? 
Itu artinya Program C# yang developernya buat tak diselamatkan menggunakan penjinaknya! 

Makanya nama modulnya *Exceptions* (Kecualian yang tidak diharapkan).

## Jaring Pengaman Try Catch

Disinilah tempat kamu ngurung error bahaya seperti Download Gagal atau Data ketuker tipe. Sama persis kaya Javascript & Pythong yang udah lu katam.

```csharp
using System;

class Program {
    static void Main() {
        Console.WriteLine("Aplikasi Windows Berjalan..");
        
        try {
            // Kita iseng aja bagi duit ghoib. ANGKA APAPUN DIBAGI NOL MESTI MELEDAK.
            int ghoib = 50 / 0; 
            
            Console.WriteLine("Beres terbagi! hasil: " + ghoib);
            // ^ GA AKAN KESENTUH KARENA JATUH KEBAWAH DULUAN
            
        } catch (DivideByZeroException e) {
            
            // Jaring jebakan spesifik kalau bener bener cuman diakalin angka 0!
            Console.WriteLine("[AMANKAN SISTEM] Lu gila dilarang ngebagi nol lahh!!");
            Console.WriteLine("Penyebab error dari Mesin: " + e.Message);
            
        } catch (Exception fatalAll) {
            
            // Jaring lebar Sapu bersih semua jenis Error!! (File ga ketelak, internet putus, dll)
            Console.WriteLine("Ada bahaya tak tersentuh: " + fatalAll.Message);
            
        } finally {
            
            // Block mulia yang selalu hidup bagaimanapun status errornya diatas td
            Console.WriteLine("-- Bersihkan Memory Card, Tutup File --");
        }
        
    }
}
```

Sekarang Program Desktop KASIR mu tidak akan Auto-Close (FC) / menghilang begitu saja di depan Bos Toko kalau ada bug tipikal receh!

---
[⬅️ Sebelumnya: LING Magic](../09-LINQ-Collection/README.md) | [🏠 Daftar Isi Utama](../README.md)
