# 10 - Membelah Arsip dengan Header (`.h`) Modern

Kalian pasti ngerjain project sampai belasan ribu baris kalau Class dicampur sama `main.cpp`. C++ Punya kebiasan Kultur Pemilahan Arsip yang unik. Semua Class **Dipisah Menjadi 2 Belahan**. Setengah Header, Setengah Badan Fungsi.

## 1. File Kepala Kop (Header) `robotku.h`

Isi file header `.h` ini HANYA UNTUK DEKLARASI DAFTAR ISI apa aja fungsi dan var yg dimilikiy tanpa menulis logic `cout` blablabla jeroannya. Kayak Daftar Menu makanan restoran kosong ga ada nasinya.

```cpp
// isi file robotku.h
#pragma once // Mantra biar di load cmn murni 1x ke harddisk
#include <string>

class KsatriaBajaHitam {
    private:
        int TenagaListrik;
        
    public:
        std::string ModelRangka;

        // CUMA JUDUL AWALAN! GAK ADA JEROAN { }
        KsatriaBajaHitam(std::string model); 
        void TebasAlien(); 
};
```

## 2. File Daging Implementasi Sebenarnya `robotku.cpp`

File `.cpp` kedua ini yang jadi pusat isiannya. Mengambil deklarasi tadi dan mengisinya. Harus nyebut Namespace Classnya biar nyambung : `NamaClass::NamaFungsi` .

```cpp
// isi file robotku.cpp
#include <iostream>
#include "robotku.h" // Tarik judul menunya dari file header tadi!

// BARU DISINI KITA ISI JEROAN DAGING CARA KERJANYA DARI FUNGSI TADI :

KsatriaBajaHitam::KsatriaBajaHitam(std::string model) {
    ModelRangka = model;
    TenagaListrik = 100;
}

void KsatriaBajaHitam::TebasAlien() {
    std::cout << "Hyattt!!!" << std::endl;
}
```

## 3. Berlayar Murni di `main.cpp`
```cpp
// main.cpp nya cuman bersisa import sebaris!!

#include "robotku.h"

int main() {
    KsatriaBajaHitam pahlawanKita("RX-78");
    pahlawanKita.TebasAlien();
    
    return 0;
}
```

Dengan menguasai arsip *Header*, selamat kawan, kamu sudah sangat siap dan pantas memasuki gerbang studio pabrik penciptaan AAA Class Game Engine Dunia manapun yang bertebaran!!

---
[⬅️ Sebelumnya: Try Catch Error Handling](../09-Error-Exception/README.md) | [🏠 Daftar Isi Utama](../README.md)
