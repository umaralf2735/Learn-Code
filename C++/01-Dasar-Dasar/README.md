# 01 - Dasar-Dasar C++ (Anak Leluhur yang Sempurna)

Jika Bahasa C sangat sakti berkat kedekatannya secara ghaib pada Hardware CPU mu, C++ diciptakan untuk menambahkan rasa Object-Oriented dari Java dan Javascript kearah C. Menjadikannya jauh lebih ramah di mata manusia!

Inilah bahasa Ibu para developer **Unreal Engine 5** kelas dunia!

## 1. Header `iostream` (Selamat Tinggal Kekerasaan C!)

Kamu benci menulis tag `%d` `%f` di PrintF nya C? Bersyukurlah C++ memperkenalkan `cout` (Console Output).

```cpp
// Sediakan Pompa aliran sungai data masuk dan keluar PC:
#include <iostream>

// Supaya ga ngetik 'std::cout' kepanjangan capek:
using namespace std;

int main() {
    int sisaPeluru = 90;
    string namaSenjata = "Meriam Bazoka"; // GOKIL C++ PUNYA STRING BENERAN!
    
    // Mengaliri layarmu layaknya aliran arus Air `<<`
    // Tanda endl artinya (End of Line / Enter otomatis)
    cout << "Karakter nembak pakai " << namaSenjata << endl;
    cout << "Aduh... Peluru sisa: " << sisaPeluru << " biji doang!" << endl;

    return 0;
}
```

## 2. Input Keyboard ( `cin` )

Meminta tulisan masuk di C++ tidak lagi membuatmu frustrasi pakai parameter aneh. Cukup `cin` (Console IN). Arah kurungnya mengarah masuk `>>` ke variabel.

```cpp
#include <iostream>
using namespace std;

int main() {
    string idUser;
    
    cout << "Sebutin Nickname Game Lu: ";
    cin >> idUser; // Otomatis mengisi text idUser diatas!
    
    cout << "Mantap Login... Halo " << idUser << endl;

    return 0;
}
```
Indah bukan bahasa buatan Bjarne Stroustrup ini?
---
[Lanjut ke Struktur Kontrol ➡️](../02-Struktur-Kontrol/README.md) | [🏠 Daftar Isi](../README.md)
