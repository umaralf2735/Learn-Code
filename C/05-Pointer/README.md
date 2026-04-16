# 05 - Pointers (Si Jantung Memori Bahasa C)

Ini dia... Selamat datang di boss penunggu dan seleksi alam bagi seluruh *programmer* dunia: **Pointer**. Kalau di Golang kita meminjam konsep simpelnya, maka di bahasa C konsep ini adalah pilar utamanya.

## 1. Alamat Memori (RAM)

Setiap variabel yang kamu cetak itu disimpan si OS dalam loker kosong bernama Alamat RAM (bentukannya aneh seperti hexadecimal: `0xFF3A12`).

Bila kamu meletakkan ampersand `&` di depan variabel, C tak akan mengambil *isinya*, dia malah memfotokan "Plang nomer rumah"-nya!

```c
#include <stdio.h>

int main() {
    int skor = 90;

    // Mari cetak skor biasa 
    printf("Isi skor: %d\n", skor); // 90

    // Mari cetak plang nomer rumahnya! (%p dipakai sbg pointer flag display)
    printf("Alamat memori RAM milik skor: %p\n", &skor); 
    // Bisa keluar huruf rahasia misal: 0x7ffe102c42ec

    return 0;
}
```

## 2. Pointers (Sang Penunjuk Arah)

Pointer adalah tipe variabel unik khusus yang tugas utamanya HANYA SATU: Nampung/Numpang nyimpen letak alamat memori (`&`) milik variabel lain. 

Kombinasi pamungkas:
- `&` : Ambilkan Alamatnya.
- `*` : Jika waktu deklarasi (arti: Aku adalah Pointer), jika di pake nanti waktu jalan (arti: Bongkar alamatnya untuk ngambil ISINYA!). Disebut juga *Dereference*.

```c
#include <stdio.h>

int main() {
    int uang = 1000;
    
    // 1. Memerintah pointer bernama ptr_ku untuk menyadap alamat laci Uang.
    int *ptr_ku = &uang; 

    // 2. Sekarang kita lihat isinya ptr_ku
    printf("Tugas saya menyimpan alamatnya, ini dia: %p\n", ptr_ku);

    // 3. Waktunya eksekusi membongkar nilai aslinya dari jarak jauh!
    printf("Ngupas pakai *, Coba tengok isi lemarinya: %d\n", *ptr_ku); 
    
    // 4. MENGUBAH MEMORI TANPA MENYENTUH VARIABEL UANG NYA!
    *ptr_ku = 5000; // Bongkar dan timpa!
    
    printf("Jeng jeng jeng... uang skrg berubah jadi: %d\n", uang); 
    // MUNCUL KEJUTAN => uang sekarang isinya 5000!!

    return 0;
}
```

Disinilah keseruannya C, kamu bisa merangkai jaringan pointer penunjuk arah yang nge-hack isian RAM sana sini tanpa harus men-duplikat memori yang membebani PC.

---
[⬅️ Sebelumnya: Fungsi](../04-Fungsi/README.md) | [Lanjut ke Algoritma Rawan ➡️](../06-Algoritma-Dasar/README.md) | [🏠 Daftar Isi](../README.md)
