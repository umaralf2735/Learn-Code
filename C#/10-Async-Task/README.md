# 10 - Asynchronous (`async` & `await`)

Mengambil data dari Database atau nunggu Network Api berdetik-detik lamanya DILARANG KERAS dilakukan di jalur utama/main-thread karena akan bikin layar PC NGELAG MACET/Not-Responding!

C# adalah pencipta asli dari pola dewa `await` (yang akhirnya dicuri/ditiru dan diadaptasi sama Javascript).

```csharp
using System;
using System.Threading.Tasks; // WAJIB!

class Program {
    
    // TAMBAHKAN async SECARA EXPLICIT.
    // Jika mau ngereturn String, bungkus pakai Task<string>.
    static async Task<string> DownloadMateriGaib() {
        Console.WriteLine("Otw Download File Rahasia CIA... (Tunggu 3 Detik ya)");
        
        // TUNDA MURNI (Mirip sleep, tapi mesin lain tetep bisa kerja)
        await Task.Delay(3000); 
        
        return "Ini file rahasianya!";
    }

    // MAIN HARUS TIPE ASYNC TASK JUGA JIKA MAU PAKE AWAIT DALEMNYA!
    static async Task Main() {
        
        // TUNGGU DENGAN SANTUY (AWAIT)
        string isi = await DownloadMateriGaib();
        
        Console.WriteLine("BERHASIL DITARIK: " + isi);
    }
}
```

Selamat! Lu sudah ngelibas The Big Boss dari Microsoft! Bahasa C# ini sangat mewah dan disukai berbagai level programmer.

Kuat banget buat Backend Server (ASP.NET), Game (Unity), bahkan Desktop App form biasa (WPF). Silahkan menjejaki dunia .NET Core sesungguhnya dan raih karir cemerlang di software enterprise dunia!!
---
[⬅️ Sebelumnya](../09-Delegate-Events/README.md) | [🏠 Daftar Isi C# Utama](../README.md)
