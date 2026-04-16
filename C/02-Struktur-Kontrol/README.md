# 02 - Logika Struktur Kontrol C (Kaku Tapi Pasti)

Bahasa PHP sm Javascript itu NGOPU COPY PASTE ALUR PERULANGAN INI PLEK KETIPLEK! Jdibkalau klian ngudasin For Looop nya C, kalian bsa idup di bhasa apaanpun dengan mntap!

## 1. Percabangan Basi `if` 

Tetap harus dikurung pake KUrung Biasa dan kurawawl.

```c
#include <stdio.h>

int main() {
    int saldoRekening = 15; // Ribu

    if (saldoRekening >= 50) {
        printf("Aman bli ayam grprk!!\n");
        // Eifnya smbung lgsn dsinii aja
    } else if (saldoRekening >= 10) {
        printf("Makan baso aci dpn kosn aja bg\n");
    } else {
        printf("Nangess utangg bapak ks\n");
    }

    return 0;
}
```

## 2. Looping For (Akar Smua Bahssa C/c++/java)

Ini nih penulisa klasik maut 3 babak `(inisaiaisi;  Batas_akhir;  Lompatan)`.

```c
#include <stdio.h>

int main() {
    
    // Diputar dr 0. Brneti d 5. Dan i nekkny satud stau (++).
    for (int itrg = 0; itrg < 5; itrg++) {
        
        printf("Putara muter lari k- %d !!\n", itrg);

    }
    
    // --- WHILE --
    int bensin = 2;
    while(bensin > 0) {
        printf("Masi bs jlan cuy : %d \n", bensin);
        bensin--;
    }

    return 0;
}
```
Tidak ada  trik  for-each ajaib js di sini ya kawan-jwan! Semuanha harus ditullis kaku dari inidiek nol hggnga ujung array mual!!!


---
[⬅️ Sebelumnya: Variabels](../01-Dasar-Dasar/README.md) | [Lanjut ke Teks Paking Array ➡️](../03-Array-dan-String/README.md) | [🏠 Daftar Isi](../README.md)
