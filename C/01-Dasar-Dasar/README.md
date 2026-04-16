# 01 - Dasar-Dasar Bahasa C

Karena umur bahasa C sudah tua (dibuat tahun 1970-an), aturannya lumayan "kuno" namun super ringan dan super ngebut (paling cepat disbanding Golang, JS, dll).

Kode bahasa C (contoh: `main.c`) tidak bisa langsung dijalanin. Dia harus "diterjemahkan" dulu sama yang namanya **Compiler** (misalnya GCC) menjadi file biner / `.exe` supaya dimengerti mesin.

## 1. Tulisan Pertamamu

Di C, struktur wajibnya mengharuskan kita memanggil *Library / Header* dasar, dan punya satu fungsi sentral bernana `main()`.

```c
#include <stdio.h> // Library: Standard Input Output (buat bisa nge-print tulisan)

int main() {
    // printf berguna untuk mencetak sesuatu
    // Jangan lupakan tanda titik koma (;) di akhir tiap baris proses!
    printf("Halo Dunia Murni!\n"); 
    
    return 0; // Mengabarkan OS (Sistem Operasi) bahwa program tamat tanpa Error.
}
```

## 2. Variabel & Tipe Data

Tidak seperti JS gampang ditebak, karena memori diatur sangat ketat, mau bikin kotak / variabel harus sebutkan tipe data yang sangat teliti.

- `int` -> Angka Bulat (misal 5)
- `float` -> Angka Desimal (misal 3.14)
- `char` -> CUMA 1 HURUF tunggal! Dipakai petik satu (misal `'A'`)
- (Mana tipe *String*? Gak ada bawaannya di C! Nanti dijelaskan di bab Array).

```c
#include <stdio.h>

int main() {
    int umur = 20;
    float berat = 65.5;
    char golongan_darah = 'O';

    // Cara print-nya unik, kamu pake "Kode Format" khusus.
    // %d = int | %f = float | %c = char
    printf("Umurku: %d tahun.\n", umur);
    printf("Beratku: %.1f kg dan gol darah %c.\n", berat, golongan_darah);

    return 0;
}
```

## 3. Input dari Keyboard (Menggunakan `scanf`)

Kalau mau memasukkan data dari *user*:

```c
#include <stdio.h>

int main() {
    int angkaFavorit;

    printf("Masukkan angka favoritmu: ");
    
    // Scanf digunakan untuk menyedot jawaban user
    // WAJIB pake simbol '&' (Pointer) didepan nama variabel saat nyedot!
    scanf("%d", &angkaFavorit); 

    printf("Wah, angka favoritmu ternyata %d!\n", angkaFavorit);
    return 0;
}
```

---
[Lanjut ke Struktur Kontrol ➡️](../02-Struktur-Kontrol/README.md) | [🏠 Daftar Isi](../README.md)
