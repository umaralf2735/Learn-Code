# 03 - Array dan String

Kita perlu tempat penitipan majemuk untuk menyimpan sekumpulan data dengan tipe identik (semuanya *int* atau semuanya *float*).

## 1. Array Satu Dimensi

Berbeda dengan array JS/Ruby yang otomatis melar (berubah size layaknya kantung doraemon), di bahasa C array itu **UKURANNYA KAKU/TETAP!** Kalau kamu mesen kardus buat 5 laci, selamanya ia 5 laci dan gaboleh lebih.

```c
#include <stdio.h>

int main() {
    // Memesan lokasi memori untuk 5 buah integer
    int laci_nilai[5];

    laci_nilai[0] = 80; // Ingat, program komputer selalu index awalnya 0!
    laci_nilai[1] = 90;
    // ...
    
    // Atau cara cepatnya:
    int plat_kendaraan[] = {1234, 4321, 5678, 8765};
    
    printf("Plat pertama: %d\n", plat_kendaraan[0]);

    return 0;
}
```

## 2. String (Realita Pahit)

Seperti yang dijanjikan, C tidak mempunyai kata ganti tipe data `string`. Di C, teks itu diakalin jatuhnya sebagai *Kumpulan Huruf* alias Array-nya `char`.

Setiap kumpulan karakter String wajib ditutup dengan *"Karakter Penamat / Null Terminator"* alias `\0`.

```c
#include <stdio.h>

int main() {
    // Menyimpan string "Halo" (Pesan ukuran 5, ingat 1 dipakai untuk penutup rahasia '\0')
    char kataSapaan[5] = {'H', 'a', 'l', 'o', '\0'};

    // Tapi untungnya pembuat compiler nambahin format langsung cepat seperti ini:
    char namaLengkap[] = "Dimas Setiawan";

    // Format print-nya kalau mau nyetak beruntun / array char adalah '%s'
    printf("Pesanku: %s\n", kataSapaan);
    printf("Namaku: %s\n", namaLengkap);

    return 0;
}
```

Mau modifikasi string? Agak berat karena dilarang pake sistem `namaLengkap = "Yanto"` gitu aja. Kalian harus panggil bantuan perpustakaan tambahan khusus: `#include <string.h>` dan gunakan rutin buatan `strcpy()` (*string copy*).

---
[⬅️ Sebelumnya: Struktur Kontrol](../02-Struktur-Kontrol/README.md) | [Lanjut ke Fungsi ➡️](../04-Fungsi/README.md) | [🏠 Daftar Isi](../README.md)
