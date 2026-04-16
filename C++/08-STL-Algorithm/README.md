# 08 - Beribadah Kepada STL (Standard Templates)

Ngetik panjang panjang ngurutin Array List Bubble Sort manual pake 2 for i dan the j di materi C tadi bikin pegel ngetik ga sih?

Selamat! Para pengarang kompiler C++ dunia ngasih kalian Perpustakaan Gratis Sakti berisi jutaan trik Algortima namanya STL (Algortihtm Template Library).

## Tinggal Masukin Mantra Sort 1 Baris

Awas, masukin include `<algorithm>` di ujung script atas dulu.

```cpp
#include <iostream>
#include <vector>
#include <algorithm> // 🌟 INI DIA PUSTAKA PARA DEWA

using namespace std;

int main() {
    vector<int> keranjangKoin = { 500, 100, 1000, 50, 200 };
    
    cout << "Koin Acak Parah! Mari kita rapihin dr miring kecil..." << endl;
    
    // GILA 1 BARIS AJA BOS SORTINGNYA
    // Cukup lempar Start Posisi Array (begin) & End Buntutnya (end)
    sort(keranjangKoin.begin(), keranjangKoin.end());
    
    cout << "Jeng Jeng!!! Jd begini: " << endl;
    
    // Terbukti rapi urut bosque
    for (int k : keranjangKoin) {
        cout << k << " rp" << endl;
    }
    
    return 0;
}
```

Sihir STL yang paling sering diapakai juga di dunia nyata:
- `find(...)` -> Nyari data ngilangin Loop for 1 1 manual
- `reverse(...)` -> Mbalik isi array sungsang otomatis.
- `max_element(...)` -> Tentukan Juara nilai 1 diantara jutaan array ga usah ngecek per if.

---
[⬅️ Sebelumnya: Pewarisan](../07-Inheritance-Polymorphism/README.md) | [Lanjut ke Try Catch Bom ➡️](../09-Error-Exception/README.md) | [🏠 Daftar Isi](../README.md)
