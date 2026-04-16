# 04 - Fungsi di C (Functions)

Ketika baris koding di `main()` mu sudah sangat tebal dan ribet (Spaghetti Code), itu pertanda mutlak kamu harus men-subsidi rutinitasnya manjadi suatu blok "Fungsi".

## 1. Merancang Fungsi Sendiri

Fungsi harus diset "Kembaliannya" tipe apa. Kalau tidak mengembalikan apa-apa (hanya nyetak di layar murni), beri tulisan tipe data `void` (Bahasa Inggrisnya hampa).

```c
#include <stdio.h>

// Fungsi Hampa / Tidak Punya Kembalian Hasil Buat diolah
void sapa_penonton() {
    printf("Halo selamat mencoba!\n");
}

// Fungsi yang Mempunyai Kembalian Integer
int tambahkanDua(int a, int b) {
    int total = a + b;
    return total;
}

int main() {
    sapa_penonton(); // Cara Manggil Fungsi Void
    
    // Cara Manggil Fungsi yang ada Return Vallenya (Bisa dimasukin variabel)
    int hasil_nambah = tambahkanDua(5, 5);
    
    printf("Nambah hasil dpt %d", hasil_nambah);
    return 0;
}
```

## 2. Penyakit Utama Fungsi: Deklarasi Susunan Bawah!

Compiler bahasa C itu membaca dari baris paling Atas ke Bawah. 
Artinya kalau fungsi `main()` nya di atas, dan fungsi buatanmu `tambahkanDua()` di taruh di bawah **SETELAH** main, Compiler bakal nangis ngeluarin Error marah-marah ("Aku ga kenal siapa tambahkanDua, belum pernah liat!").

Solusinya: Gunakan teknik **Function Prototype**. (Nyebur namanya duluan).

```c
#include <stdio.h>

// Kasih bocoran dulu ke C bahwa fungsi ini ADA, definisinya nanti dibawah belakangan boss
int kurangiMundur(int a, int b);

int main() {
    // Karena udah dikasih bocoran, si main() ga bakal protes pas make!
    int ans = kurangiMundur(10, 2); 
    printf("Ans = %d", ans);
    return 0;
}

// Baru dijabarin komplit di bawah!
int kurangiMundur(int a, int b) {
    return a - b;
}
```

---
[⬅️ Sebelumnya: Array dan String](../03-Array-dan-String/README.md) | [Lanjut ke Pointer (WAJIB BACA!) ➡️](../05-Pointer/README.md) | [🏠 Daftar Isi](../README.md)
