# 02 - Struktur Kontrol Pola C-Family

Karena sifat bahasa Ibu adalah C, maka C++ 100% menggunakan arsitektur struktur kondisi yang sama.

## 1. Pengecekan If Murni Mutlak

Berbeda dengan jaman now Python yg tak pake kurung. Di C++ hukum C tetap jalan.

```cpp
#include <iostream>
using namespace std;

int main() {
    int darahMusuh = 0;
    
    if (darahMusuh > 50) {
        cout << "Musuh tebel abis!" << endl;
    } else if (darahMusuh > 0) {
        cout << "Terus pukul dikit lagi mati tu!!" << endl;
    } else {
        cout << "YOU WIN CONGRATS!! LOOT DROPPED!!" << endl;
    }

    return 0;
}
```

## 2. Looping

Loop For biasa seperti ini.
```cpp
// Mencetak bintang bersusun
for(int bintang = 1; bintang <= 3; bintang++) {
    cout << "Bintang jatuh ke - " << bintang << endl;
}
```

Loop do-while (Bedanya ini diluar nalar. Dia "Main tabrak eksekusi dulu minim sekali. Kalo syarat baru nyadar ga cocok mskipun diulang di tarikan kdua nya bakal disetop!")

```cpp
int uangKoin = 0;

do {
    cout << "Mesin menelan koin (Meskipun Koin Ku ternyata " << uangKoin << ") .." << endl;
    uangKoin++;
} while (uangKoin < 0);

// Bayangkan!!! Padahal koin gw cuman 0 !! Tp dia nyolong nyedot ngeprint sekali wih!
// Kalo pake WHILE biasa dari awal ga bakal kesentuh wkwk!
```

---
[⬅️ Sebelumnya: Dasar Dasar](../01-Dasar-Dasar/README.md) | [Lanjut ke Vector ➡️](../03-Array-Vector/README.md) | [🏠 Daftar Isi](../README.md)
