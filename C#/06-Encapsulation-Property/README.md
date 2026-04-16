# 06 - Encapsulation & Properties Rahasia

Di Bab sebelumnya kita makai tulisan `public string Nama;`. Itu bahaya bos! Kalau data KTP tiba-tiba di ganti sama class orang lain kan Kacau?

Konsep aslinya adalah Variabelnya disihir menajadi Rahasia (`Private`). Terus kita siapken pintunya secara hati-hati pakai Function (`Get` dan `Set`). Di bahasa C# dan C++, itu dinamakan **Encapsulation (Pembungkusan)**.

## Properti Auto-Sakti punyanya C# (`get; set;`)

Bila di Java kalian harus nulis fungsi manual bergulung layar `public String getKTP() { return KTP; }` dll. Di C#... Lihatlah seninya Tuan Tuan:

```csharp
class AkunGame {
    
    // VARIABEL TRADISIONAL C++ TUA (Ngasih Kunci Getter Penuh)
    private int nyawaRahasia = 100;
    public int AmbilNyawa() {
        return nyawaRahasia;
    }
    
    // FITUR MEWAH C# PROPERTY NYA!!
    // Dia cuman public luar keliatan, tapi waktu NGEDIT nyawa (Set), dia private/dikunci otomatis!
    public int Armor { get; private set; }
    
    // Paling enak ini, Kasi Public baca dan tulis, tapi logic tersembunyi
    public string Namapanggilan { get; set; }

    public AkunGame() {
        // Nyetel nilai yg diprivate di dalam rumahnya (Boleehhh!)
        Armor = 50;
        Namapanggilan = "SopoJarwo";
    }
}


class Program {
    static void Main() {
        AkunGame orangKu = new AkunGame();
        
        // Console.WriteLine( orangKu.nyawaRahasia  );  // ❌ MERAH! RAHASIA!
        
        Console.WriteLine( orangKu.Armor );  // ✔️ Output: 50
        
        // orangKu.Armor = 90; // ❌ ERROR! NGEDitNYA KAN UDAH LU PRIVATE MANIS TADI!
        
        // BISA BACA DAN BISA NUMPANG NULIS JUGA! PAKE GET SET!
        orangKu.Namapanggilan = "GantiNamaAja";
    }
}
```

Keren abis yak! Diatas adalah contoh C# mengalahkan kepelikan penulisan OOP Java yang bertele-tele.

---
[⬅️ Sebelumnya: Dasar Class](../05-OOP-Class-Object/README.md) | [Lanjut ke Pewarisan Darah ➡️](../07-Inheritance-Polymorphism/README.md) | [🏠 Daftar Isi](../README.md)
