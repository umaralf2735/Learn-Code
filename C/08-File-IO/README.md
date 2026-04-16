# 08 - Berkomunikasi dengan File (File I/O C)

Basa C memiliki kemampuan menulis isi Log langsung ke komputermu, layaknya menyimpan history perbankan.
I/O C berfokus pada Penggunaan Pointer File `FILE *` khusus.

## Menulis ke Berkas `fprintf`

Mode file yang kita pakai adalah `w` (Write). Mode ini akan menimpa file apabila sudah ada, dan membuatnya jika file tersebut belum lahir di komputermu.

```c
#include <stdio.h>

int main() {
    
    // Gantungkan Pointer khusus bertipe FILE
    FILE *bukuSakti = fopen("baca_aku.txt", "w");
    
    // Safety Net (Pengaman jika Hardware rusak/Penuh)
    if (bukuSakti == NULL) {
        printf("Astaga! File Gagal Terbuat!");
        return 1;
    }
    
    // Menulis kedalam dengan fprintf (File Print Formatted)
    fprintf(bukuSakti, "Halo Komputer!\n");
    fprintf(bukuSakti, "Uang nasabah telah diamankan: %d\n", 999120);
    
    // JANGAN LUPA DITUTUP! JIKA TIDAK AKAN CORRUPT/BOCOR MEMORY!
    fclose(bukuSakti);
    
    printf("Sukses nulis berkas!\n");

    return 0;
}
```

Bisa dibayangkan bukan betapa raw dan rapinya penulisan ini dibalik layar bahasa pemrograman modern saat ini yang kamu pakai sehari-hari.
---
[⬅️ Sebelumnya](../07-Struct-dan-Memori/README.md) | [Lanjut ➡️](../09-Preprocessor/README.md) | [🏠 Daftar Isi](../README.md)
