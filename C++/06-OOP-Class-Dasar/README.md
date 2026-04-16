# 06 - Kasta Dewa: OOP Murni C++

C tidak punya blueprint Class. C++ menyuntikkan nyawa Class menjadi fondasi terberat dan terminumnya. Semua game engine modern dibentuk dari OOP C++.

## Sintaks Blueprint Class

Gak kaleng-kaleng, di C++ kita pisah jelas mana baris buat nulis sifat internal rahasianya (Data) dan tindakan yang dibolehkan untuk dilihat Publik!
Jangan lupakan titik koma mutlak `;` menancap diujung penutup kurung tutup.

```cpp
#include <iostream>
using namespace std;

// MEMBUAT CETAKAN (Blueprint Kucing)
class KucingMimpi {
    // 🔒 DIKUNCI! GA ADA ORANG ATAU FILE LUAR YANG BOLEH NGEDIT ATAU TAU VAR INI!
    private:
        int nyawaRahasia;

    // 🌟 BEBAS DIAKSES/DIBACA PUBLIK!
    public:
        string julukan;
        
        // Constructor (Method yg namanya plek sama kek Class - Auto Jalan Pertama kali!)
        KucingMimpi(string nama) {
            julukan = nama;
            nyawaRahasia = 9; // Diset otomatis pas kecetak
        }
        
        void KurangiNyawa() {
            nyawaRahasia -= 1;
            cout << "Aduh keserempet ban! Nyawaku sisa: " << nyawaRahasia << endl;
        }
};

int main() {
    // Mencetak satu ekor!!
    KucingMimpi kucinGarong("Orenji"); 
    
    // kucinGarong.nyawaRahasia;   ❌ ERROR BOS! LU MO LEWAT PINTU BLAKANG?! PRIVATE TUH
    
    cout << "Hai " << kucinGarong.julukan << endl; // ✔️ Aman, Public
    
    // Kurangi darah dia lewat method publik
    kucinGarong.KurangiNyawa();
    
    return 0;
}
```

Terasa sama kayak Java dan TS? Tentu! C++ lah sesepuh mereka yang mendikte arsitektur ini.

---
[⬅️ Sebelumnya: Dinamik Pointer](../05-Pointer-Memori/README.md) | [Lanjut ke Inheritance ➡️](../07-Inheritance-Polymorphism/README.md) | [🏠 Daftar Isi](../README.md)
