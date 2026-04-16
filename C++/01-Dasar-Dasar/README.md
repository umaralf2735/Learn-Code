# 01 - Dasar Output dan Input Modern C++

Bahasa C++ sangat menyanjung "Streams" atau Aliran Data. Menggantikan si kembar tua pembuat mumet pola persen dari C (`printf` dan `scanf`).

## 1. Menulis Cetakan ke Layar (Terminal)

```cpp
// 1. Dulu kita pake stdio.h, srg diganti alat streaming I/O canggih
#include <iostream> 

// (Optional) Biar kita gausah ngetik 'std::' berulang ulang tiap manggil perabotan
using namespace std;

int main() {
    
    // cout (Character OUT = Cetak Keluar)
    // Gunakan lambang stream << untuk nyeselkin isinya
    cout << "Halo Pemain Game Unreal Engine!!" << endl;
    
    // Kalo tanpa using namespace, ngetiknya panjang kek gini:
    // std::cout << "Gila capek bos" << std::endl;
    
    return 0;
}
```

## 2. Menyedot Input Interaktif

Ajaibnya dari C++, kamu ngga perlu pusing nulis `%d` untuk nyedot Int ato `%s` buat narik String kek kakek C mu!

```cpp
#include <iostream>
using namespace std;

int main() {
    int nomerSepatu;
    
    cout << "Eh bos, ukuran sepatumu rapa? ";
    
    // Membaca ketikan user pake perintah cin (Character IN)
    // Tanda alirannya keBALIK masukan KEDALAM variabel ( >> )
    cin >> nomerSepatu;
    
    // Otomatis nyatuin text + variable tanpa pake koma koma ribet printf C
    cout << "Gila gede amat nomernya " << nomerSepatu << " yah!" << endl;

    return 0;
}
```

---
[Lanjut ke Struktur Kontrol ➡️](../02-Struktur-Kontrol/README.md) | [🏠 Daftar Isi](../README.md)
