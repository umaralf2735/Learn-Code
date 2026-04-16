# 09 - Preprocessor (#define)

Pernahkah kamu memperhatikan baris awal di program C selalu diawali dengan tanda Pagar `#`?
Ini disebut Preprocessor. Preprocessor adalah perintah khusus yang akan dibaca pertama kali oleh Compiler BARENGAN sebelum kodemu diubah jadi mesin.

## 1. Konstanta Macro Ajaib
Kamu bisa menggunakan preprocessor untuk menggantikan seluruh teks kodinganmu dengan gila-gilaan, bagaikan fitur Find and Replace otomatis MS word.

```c
#include <stdio.h>

// BACA: Ubah setiap detak kata PAJAK_NEGARA menjadi angka mitsisnya
#define PAJAK_NEGARA 0.15

// Macro bisa berbentuk fungsi buatan mini tanpa kurung kurawal!
#define GANDAKAN(a) (a * 2)

int main() {
    float uangAsli = 50000;
    
    // Compiler akan merubah kata PAJAK_NEGARA menjadi 0.15 sebelum dieksekusi secara ghaib!
    float terpotong = uangAsli * PAJAK_NEGARA; 
    
    printf("Setelah Pajak: %f \n", terpotong);
    
    // Memutar Fungsi Ghaib Macro:
    printf("Pukulan Ganda: %d \n", GANDAKAN(20));
    
    return 0;
}
```
---
[⬅️ Sebelumnya](../08-File-IO/README.md) | [Lanjut ➡️](../10-Error-Handling/README.md) | [🏠 Daftar Isi](../README.md)
