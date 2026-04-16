# 09 - Preprocessor (`#define` & Macro)

Sadar gak kamu dari kemarin selalu buka kode pakai tulisan `#include` ? Kode awal bermartabat tagar (`#`) di C tidak diproses waktu program kamu dijalanin *Realtime*. Ia dibaca "Bahkan Sebelum Disaring Oleh Compiler" (Pra-proses).

## 1. Konstanta Murni (`#define`)

Kalau di Golang / JS ada `const`. Di C kita paling disarankan menulis konstanta mutlak menggunakan Macro define.
Keunggulannya, *C* akan melakukan metode **"REPLACE ALL (Copy Paste Massal Se-Dokumen)"** menukarin nama dengan angkanya ke seantero script. Jadi ini sangaaat menghemat ngos-ngosan RAM!

```c
#include <stdio.h>

// MACRO DITETAPIN DILUAR FUNGSI MAIN()
#define PHI 3.14
#define BAHASA "Indonesia Raya"

int main() {
    // Si compiler pada detak detik 0 bakal menghapus kata PHI 
    // diganti angka 3.14 murni tanpa lewat register variable apapun
    float luas = 5 * 5 * PHI; 
    
    printf("Luas %f dengan bahasa %s", luas, BAHASA);
    
    return 0;
}
```

## 2. Macro Berbentuk Fungsi Sintetis Lintas Batas

Kamu bisa nulis rumus di define juga!

```c
#include <stdio.h>

#define MAKSIMUM(A, B) ((A > B) ? A : B)

int main() {
    int juara = MAKSIMUM(10, 50);
    printf("Nilai terbesarnya: %d", juara); // Output: 50
    return 0;
}
```
Ini bukan Method asli. Macro hanya modal *copas* sehingga kecepatannya brutal. Trik ini sangat sering dipakai pada sistem tertanam (IoT / Arduino Programmer pasti sering make).

---
[⬅️ Sebelumnya: File I/O](../08-File-IO/README.md) | [Lanjut ke Error Handling ➡️](../10-Error-Handling/README.md) | [🏠 Daftar Isi](../README.md)
