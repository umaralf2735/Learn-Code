# 10 - Penanganan Error (No Try Catch!)

Python punya Try-Except. Javascript punya Try-Catch.
Bahasa C? **TIDAK PUNYA!**

C memaksamu membiasakan diri mengecek setiap hasil dari fungsi dan mengambil tindakan manual.

## 1. Pengecekan Error Bawaan (`errno`)

Library error C menggunakan mekanisme status kode yang selalu ditimpa ke alamat nomor memori.

```c
#include <stdio.h>
#include <errno.h> // Wajib di panggil
#include <string.h>

int main() {
    
    // Sengaja buka file antah berantah agar gagal!
    FILE *cobaBuka = fopen("file_ini_gabakal_ada_bro.txt", "r");
    
    // Pengecekan Manual Tanpa Try Catch!
    if (cobaBuka == NULL) {
        
        // Panggil fungsi PERROR (Print Error). OS Akan berteriak mencetak Alasan Kegagalan!
        perror("GAGAL TOTAL BOS: ");
        
        // KITA HARUS BALIKKAN ANGKA ERROR NON-NOL MURNI! AGAR WINDOWS TAHU PROGRAM KITA HANCUR!
        return 1; 
    }
    
    printf("File Berhasil!\n");
    fclose(cobaBuka);
    return 0;
}
```

Disinilah perjalananmu dengan leluhur sistem operasi berakhir!
Pergilah menjelajah C++ yang lebih Modern untuk Pembuatan Game AAA.
---
[⬅️ Sebelumnya](../09-Preprocessor/README.md) | [🏠 Daftar Isi C Murni](../README.md)
