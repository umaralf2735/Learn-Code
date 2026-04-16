# 03 - Vectors (Dewa Array Melarnya C++)

Kenapa C murni tidak bisa dimasukkan Array sesuka hati yang melentur panjang seperti peluru Game RPG yang tak terbatas pelurunya?
Karena Array biasa bersifat statis di ukuran!

Masuklah `std::vector<>`. Ini adalah list ajaib buatan C++ STL yang bisa memanjang tak terhingga ukurannya ketika di PUSH layaknya javascript!

```cpp
#include <iostream>
#include <vector> // WAJIB DIIMPORT UNTUK BISA PAKE ILMUNYA!

using namespace std;

int main() {
    // 1. Deklarasi Vector dinamis tipe String Murni!
    vector<string> keranjangBelanja; 
    
    // 2. Gunakan Push Back untuk mengisi dari belakan!
    keranjangBelanja.push_back("Bawang Merah");
    keranjangBelanja.push_back("Telor Ayam");
    keranjangBelanja.push_back("Mie Instan");
    
    // 3. Mengambilnya sama gampangnya kayak JS: 
    cout << "Wih barang ketiga gue adlah: " << keranjangBelanja[2] << endl;
    
    // Pemutar otomatis mengiring list!
    cout << "Seluruh isi Tasku:" << endl;
    for(int idx = 0 ; idx < keranjangBelanja.size(); idx++){
        cout << "- " << keranjangBelanja[idx] << endl;
    }

    return 0;
}
```
---
[⬅️ Sebelumnya](../02-Struktur-Kontrol/README.md) | [Lanjut ➡️](../04-Pointer-dan-Ref/README.md) | [🏠 Daftar Isi](../README.md)
