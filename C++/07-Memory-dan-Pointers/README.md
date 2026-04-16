# 07 - Smart Pointers (Penyelamat Memori)

Di C murni, alokasi memori manual pakai `malloc` dan `free` (atau `new` dan `delete` di C++) rentan banget bikin *Memory Leak* jika lupa dihapus!

Masuklah `std::unique_ptr` dari C++ modern. Saat fungsi selesai, pointer ini akan MENGHAPUS DRINYA SENDIRI dari RAM!

```cpp
#include <iostream>
#include <memory> 
using namespace std;

class Monster {
    public:
        Monster() { cout << "Lahir!" << endl; }
        ~Monster() { cout << "Mati Terhapus Otomatis!" << endl; }
};

int main() {
    { // Blok scope RAM
        unique_ptr<Monster> bosAcak = make_unique<Monster>();
    } // Keluar blok ini, RAM otomatis terhapus tanpa perlu 'delete'
    cout << "Aman!" << endl;
    return 0;
}
```
---
[⬅️ Sebelumnya](../06-OOP-Lanjut/README.md) | [Lanjut ➡️](../08-File-IO/README.md) | [🏠 Daftar Isi](../README.md)
