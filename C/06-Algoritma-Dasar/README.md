# 06 - Algoritma Bubble Sort

Karena di C tidak ada fungsi ajaib `.sort()` dari luar, kita diwajibkan menulis algoritma secara manual. Ini mengasah insting logika kita.

Sebagai contoh, jika ada Array yang angkanya acak `[50, 10, 80, 2]`. Kita putar elemen dengan saling menukar tempat mereka:

```c
#include <stdio.h>

int main() {
    int tumpukan[5] = {50, 15, 99, 1, 30};
    int total = 5;

    // Loop berputar berkali kali memilah data
    for (int it1 = 0; it1 < total - 1; it1++) {
        
        for (int it2 = 0; it2 < total - it1 - 1; it2++) {
            
            // JIKA ANGKANYA LEBIH BESAR, GESER DIA KE KANAN!
            if (tumpukan[it2] > tumpukan[it2 + 1]) {
                
                // Proses Tukar tempat dengan alat bantu variabel wadah sementara:
                int tempWadah = tumpukan[it2];
                tumpukan[it2] = tumpukan[it2 + 1];
                tumpukan[it2 + 1] = tempWadah;
            }
        }
    }

    printf("Setelah Diurutkan:\n");
    for (int i = 0; i < 5; i++) {
        printf("%d, ", tumpukan[i]);
    }
    
    return 0;
}
```
---
[⬅️ Sebelumnya](../05-Pointer/README.md) | [Lanjut ➡️](../07-Struct-dan-Memori/README.md) | [🏠 Daftar Isi](../README.md)
