# 07 - Pewarisan & Virtual (Turunan Genetik)

Memiliki monster slime standar? Bagaimana kalau kamu pengen bikin King Slime yang nyerang pakai Racun? Apa bikin class baru lagi? Gak usaahh! Turunkan! Inheritance pakai lambang titik dua biasa `: mode classOrangTua`.

## Virtual, Sang Pembangkang

Kalau class Induk punya kemampuan lari pelan, maka beri gelar dia kemampuan lari **`virtual`**. Maksudnya adalah: "Hai anak-anakku, kalau kalian ga suka cara aku lari, kalian boleh timpa ubah (Override) ini saat kalian mekar!".

```cpp
#include <iostream>
using namespace std;

// --- SANG BAPAK PUSAT ALAM SEMESTA --
class Senjata {
    public:
        // PAKE VIRTUAL BIAR BISA DISEMPURNAKAN SI ANAK NANTI !!
        virtual void Attack() {
            cout << "*Mukulin musuh pake gangan kayu biasa.. Cettok!*" << endl;
        }
};

// --- ANAK SATU: PEDANG -- (Aku ngewarisi darah senjata bapakku mode public)
class Pedang : public Senjata {
    public:
        // OVERRIDE: Aku punya cara nepok sndiri pak! Gajadi nepok kayu aku pengen nebas tajem!
        void Attack() override {
            cout << "SRINGG !!! ZREESSH!! *Darah Muncret 100 DMG*" << endl;
        }
};

int main() {
    // Aku megang benda berdarah kayu bapaknya
    Senjata kayu_biasa; 
    
    // Aku nemu senjata pedang tajem
    Pedang pedang_excalibur;
    
    kayu_biasa.Attack();       // Cettokkk garing
    pedang_excalibur.Attack(); // ZRESHH!! MANTAP BEDA WALAUPUN TURUNAN
    
    return 0;
}
```

Game C++ isinya adalah hal ini di setatus ribu level file bertumpuk. Keren sekali bukan.

---
[⬅️ Sebelumnya: Class Dasar](../06-OOP-Class-Dasar/README.md) | [Lanjut ke STL Magis ➡️](../08-STL-Algorithm/README.md) | [🏠 Daftar Isi](../README.md)
