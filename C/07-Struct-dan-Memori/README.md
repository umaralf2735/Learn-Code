# 07 - Tipe Kustom Struct

Bahasa C tidak mendukung Object Oriented Programming (Kalian harus merantau ke C++ untuk itu). Namun, ia mendukung cetakan pola primitif bernama **Struct**.

## Cetakan Object Buatan Struct
Dengan struct, kalian bisa menggabungkan text, dan integer dalam 1 ikatan kelompok!

```c
#include <stdio.h>
#include <string.h>

// Bikin Cetakan Data nya dulu
struct TahananSel {
    int idBuronan;
    char namaKelompok[50];
    float lamaHukumanTahun;
};

int main() {
    // Siapkan wadah untuk mengisi data
    struct TahananSel narapidana1;
    
    // Tembak pake titik (dot notation)
    narapidana1.idBuronan = 4492;
    narapidana1.lamaHukumanTahun = 15.5;
    
    // Awas! Kamu harus pakai Strcpy khusus untuk menjejalkan String ke dalam C!!
    strcpy(narapidana1.namaKelompok, "Suhu Preman Lembang");
    
    printf("Pak Buron [%d] dari %s di sel selama %f tahun \n", narapidana1.idBuronan, narapidana1.namaKelompok, narapidana1.lamaHukumanTahun);

    return 0;
}
```
Ini adalah bekal awal kalian paham bagaimana File System dan OS berjalan tanpa harus bergantung dengan modern-oop!
---
[⬅️ Sebelumnya](../06-Algoritma-Dasar/README.md) | [Lanjut ➡️](../08-File-IO/README.md) | [🏠 Daftar Isi](../README.md)
