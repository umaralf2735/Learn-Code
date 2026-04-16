# 06 - Pewarisan & Polimorfisme (OOP C++)

Dalam C++, pewarisan menggunakan tanda titik dua `:`.  Ini sangat kuat karena memungkinkan penggunaan fungsionalitas dari class Parent ke Class Child.

```cpp
#include <iostream>
using namespace std;

// Class Induk
class Mobil {
    public:
        void bunyiMesin() {
            cout << "Brm Brmm!!" << endl;
        }
};

// Class Anak (Mewarisi Mobil)
class MobilSport : public Mobil {
    public:
        void turbo() {
            cout << "Wuuush!!" << endl;
        }
};

int main() {
    MobilSport ferrari;
    ferrari.bunyiMesin(); // Warisan dari Induk
    ferrari.turbo(); // Skill sendiri
    return 0;
}
```

Pewarisan di C++ membedakannya dari C murni dan memberikan kemudahan besar.
---
[⬅️ Sebelumnya: Class OOP](../05-Class-OOP/README.md) | [Lanjut ke Memory ➡️](../07-Memory-dan-Pointers/README.md) | [🏠 Daftar Isi](../README.md)
