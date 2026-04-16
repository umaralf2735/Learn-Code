# 04 - Reference Vs Pointer di C++

Di C, Pointers adalah hal yang wajib dipakai membongkar isi variabel di luar batasan Main / scope function dan memakan kerunyaman pengetikan * (Dereference).
Di C++, mereka menciptakan **References (`&` pada argumen)** yang tidak perlu memboroskan penulisan bintang berkali-kali!

## Kekuatan Reference `&`

```cpp
#include <iostream>
using namespace std;

// 1. TANDA & MENANDAKAN REFERENSI LANGSUNG (bukan Fotokopi)!!
void gantiNilaiLangsung(int& isiBrankas) {
    
    // GAK PERLU BINTANG (*) MURNI! Langsung Timpa Kaya Variabel anak kecil!!
    // DIA AKAN MENGUBAHNYA MENEMBUS KELUAR ARENA Main() !!
    isiBrankas = 9991200; 
}


int main() {
    int gajiiUAMRAwal = 5500;
    
    // 2. Memanggilnya Polosan Biasa! Ga perlu & di depannya lagi.
    gantiNilaiLangsung(gajiiUAMRAwal);
    
    
    // BUKTI NYATA! Gajinya telah di Hack berubah jadi 9 JUTA!!
    cout << "Hasil Hack Akhir: " << gajiiUAMRAwal << endl;

    return 0;
}
```

Reference sangat digemari karena aman (dia tidak bisa dikosongkan null), mudah mengetiknya, serta menghindari kebocoran memory dari Pointer mentah murni.
---
[⬅️ Sebelumnya](../03-Array-Vector/README.md) | [Lanjut ➡️](../05-Class-OOP/README.md) | [🏠 Daftar Isi](../README.md)
