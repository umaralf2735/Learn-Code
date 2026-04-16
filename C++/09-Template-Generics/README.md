# 09 - Template (Generics)

Template adalah fondasi C++ untuk tipe parameter gaib, mirip `<T>` di TypeScript!

```cpp
#include <iostream>
using namespace std;

// Buat template fungsi gaib
template <typename T> 
void bungkusBarang(T isian) {
    cout << "Isi tas: " << isian << endl;
}

int main() {
    bungkusBarang<int>(900); // Tipe Integer
    bungkusBarang<string>("Pedang"); // Tipe String
    return 0;
}
```
Inilah alasan `vector<string>` di C++ bisa menampung apa saja!
---
[⬅️ Sebelumnya](../08-File-IO/README.md) | [Lanjut ➡️](../10-Make-File/README.md) | [🏠 Daftar Isi](../README.md)
