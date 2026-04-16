# 04 - Fungsi & Pass by Reference (Kemewahan C++)

Waktu main pointer `*` sama `&` di bahasa C buat modif variable asli memori dari kejauhan itu ribet sekali karena kodenya banyak tanda bintangnya kesana sini.

C++ memiliki siasat rahasia yaitu **Pass By References** murni di parameternya! Tanpa sadar kita ngehack memori orang alias Tanpa Duplikat Data!

## 1. Fungsi Duplikat Pass by Value (Aman, Tapi Rakus Ram Kalau data Gede)
```cpp
#include <iostream>
using namespace std;

// (V) Versi Value: Data yg dilempar kesini diclone murni didalam kotak baru di RAM
void tambahSisaAmmo(int peluru) {
    peluru += 50; 
}

int main() {
    int isiTas = 10;
    tambahSisaAmmo(isiTas);
    
    cout << isiTas; // HASILNYA TETEUP 10!!! (Karena fungsi tadi cuma megang foto kopinya!)
    return 0;
}
```

## 2. Fitur Spesial `&` Di Kurung Parameter (Referensi Asli Mematikan C++)
Cukup tempelkan lambang `&` disamping tipe function-nya waktu deklarasi, Mendinginkan Pointer berdarah darah milik bapanya!

```cpp
#include <iostream>
using namespace std;

// (R) Cukup tambahkan & dan seakan akan ini adalah Variabel aselinya yg dikirim! 
void tukangAmbilTasBeneran(int &peluruAsli) {
    peluruAsli += 50; // Langsung terhubung ke memori utama tas dipemanggilnya!! 
}

int main() {
    int isiTas = 10;
    
    // Ga perlu dikirim dengan bintang aneh. Cukup lempar kayak biasa
    tukangAmbilTasBeneran(isiTas); 
    
    cout << isiTas; // HASIL TARA!! BERUBAH JADI 60!
    
    return 0;
}
```

Trik `&` parameter sakti ini banyak membakar jam terbang programmer pemula Game Dev yang kebingungan: "Lah kok char gw nyawanya habis sendirinya kan cumn buat baca doang ke copy di ui". Wah padahal dia lemparnya pake reference!

---
[⬅️ Sebelumnya: Vector](../03-Array-Vector/README.md) | [Lanjut ke Pointer Sakti ➡️](../05-Pointer-Memori/README.md) | [🏠 Daftar Isi](../README.md)
