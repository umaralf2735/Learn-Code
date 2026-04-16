# 03 - Array dan Karakter Murni (C)

Di bahasa C, array sangatlah kaku. Kamu tidak bisa menambah atau mengurangi ukurannya setelah diciptakan.

## 1. Array Statis
Ketika mendeklarasikan array, kamu wajib memberikan ukuran mutlaknya di dalam kurung siku `[]`.

```c
#include <stdio.h>

int main() {
    // Array isi 5 slot kembar!
    int nilaiSiswa[5] = {90, 80, 85, 70, 95};
    
    // Gak ada kata push() ! Harus ganti manual:
    nilaiSiswa[2] = 100;
    
    // Mencetak satu persatu:
    for(int i = 0; i < 5; i++) {
        printf("Nilai ke %d adalah: %d \n", i, nilaiSiswa[i]);
    }

    return 0;
}
```

## 2. Ilusi String di C
Berbeda dari Python yang punya teks String ajaib, C hanya menganggap Teks sebagai jajaran karakter tunggal (`char`) yang diakhiri dengan simbol gaib `\0` (Null terminator).

```c
#include <stdio.h>

int main() {
    // String hanyalah Array Karakter!
    char passwordAdmin[] = "Rahasia123";
    
    printf("Password lo adalah: %s \n", passwordAdmin);
    return 0;
}
```
---
[⬅️ Sebelumnya](../02-Struktur-Kontrol/README.md) | [Lanjut ➡️](../04-Fungsi/README.md) | [🏠 Daftar Isi](../README.md)
