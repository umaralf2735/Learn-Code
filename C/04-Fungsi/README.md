# 04 - Fungsi di C (Function Prototype)

Bahasan C sangat ketat terhadap posisi fungsi. Kalau kamu menaruh fungsi pembantu di bawah fungsi `main()`, komputer tidak akan mengenalinya kecuali kamu membuat "Prototype" di bagian atas!

## 1. Mendeklarasikan Tipe Balikan

```c
#include <stdio.h>

// BACA: Fungsi ini WAJIB ngeluarin Angka Int dan Menerima Int Pula
int kurangiDarah(int darahAsli, int damage) {
    int sisa = darahAsli - damage;
    return sisa;
}

// VOID = Tidak Memulangkan Nilai Apapun!
void cetakKematian() {
    printf("Ahhh! Kamu Telah Gugur di Medan Perang!\n");
}

int main() {
    int darahKu = 100;
    
    // Pemanggilan fungsi
    darahKu = kurangiDarah(darahKu, 20);
    
    printf("Sisa HP ku: %d \n", darahKu);
    
    if (darahKu <= 0) {
        cetakKematian();
    }
    
    return 0;
}
```

Jika terbiasa memakai JS, pastikan C memaksamu agar setiap kotak fungsi punya Label Tipe yang jelas!
---
[⬅️ Sebelumnya](../03-Array-dan-String/README.md) | [Lanjut ➡️](../05-Pointer/README.md) | [🏠 Daftar Isi](../README.md)
