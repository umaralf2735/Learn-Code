# 05 - Pointers (The God Mode)

Selamat datang di materi yang konon sering membuat Mahasiswa Informatika menangis!
**Pointer**.

Intinya sederhana: Pointer BUKAN nilainya, melainkan **Alamat** (Kordinat RAM) tempat nilai itu bersembunyi.

## 1. Mengintip Alamat dengan `&` (Ampersand)

```c
#include <stdio.h>

int main() {
    int uangRahasia = 50000;
    
    // Tanda & memberitahu "Dimanakah kordinat uangku disimpan?"
    printf("Uangku tersimpan di kordinat Memory: %p \n", &uangRahasia);
    
    // Hasilnya akan aneh seperti 0xFA01B dst.
    return 0;
}
```

## 2. Mengubah Nilai Jarak Jauh dengan Pointer `*` (Asterisk)

```c
#include <stdio.h>

void cheatUang(int *pointerUang) {
    // Karena kita pake * (Dereference), C akan terbang ke alamat aslinya dan MEMBONGKAR BRANKASNYA!
    *pointerUang = 999999;
}

int main() {
    int dompet = 10;
    
    // Fungsi cheat butuh alamat dari dompet tsb
    cheatUang(&dompet);
    
    // GILA! Kita ga pernah nulis dompet = 999.. di Main, tapi tiba-tiba angkanya berubah drastis!
    printf("Isi dompetku sekarang kena sulap: %d \n", dompet);
    
    return 0;
}
```

Disinilah letak kehebatan Bahasa C dalam melibas mesin langsung dengan menyedot kordinat RAM Hardware Komputermu secara mentah. Berbahaya namun Cepat Luar Biasa!
---
[⬅️ Sebelumnya](../04-Fungsi/README.md) | [Lanjut ➡️](../06-Algoritma-Dasar/README.md) | [🏠 Daftar Isi](../README.md)
