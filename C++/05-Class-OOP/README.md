# 05 - Orientasi Objek Modern (Class)

Semua arsitektur bahasa luar (Ruby, TS, PHP, Java) menuruni Class yang diperkenalkan C++. Inilah fondasi utamanya. Object disembunyikan menggunakan Private dan dibungkus properti public!

## 1. Merancang Pabrik Object C++

```cpp
#include <iostream>
using namespace std;

class PekerjaPabrik {
    // AREA PRIVAT (Gak bisa dibaca dari jangkauan Luar Class terekspos!)
    private:
        int gajiOrangDalam_Rahasia;

    // AREA LUAS (Area Terbuka Public yang membebaskan Interaksi luar)
    public:
        string namaAktePegawai;
        
        // CONSTRUCTOR: Dipanggil otomatis pertama menunggangi New Class Baru!
        PekerjaPabrik(string inputNama, int inputGaji) {
            namaAktePegawai = inputNama;
            gajiOrangDalam_Rahasia = inputGaji;
        }

        // METHOD: Aksi 
        void unjukBicara() {
            cout << "Halo saya " << namaAktePegawai << " lagi ngumpetin gaji Rp." << gajiOrangDalam_Rahasia << endl;
        }
};

int main() {
    
    // Cara panggil tidak butuh Tembelan Teks (new) lagi!
    PekerjaPabrik bapakUdin = PekerjaPabrik("Pak Udin Security", 99120000);

    bapakUdin.unjukBicara();

    // ERROR Murni!! Krn Gaji privat gak bsa dijebol
    // bapakUdin.gajiOrangDalam_Rahasia = 999; 

    return 0;
}
```
---
[⬅️ Sebelumnya](../04-Pointer-dan-Ref/README.md) | [Lanjut ➡️](../06-OOP-Lanjut/README.md) | [🏠 Daftar Isi](../README.md)
