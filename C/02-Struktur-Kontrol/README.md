# 02 - Struktur Kontrol C

Logika percabangan sangat generik dan mirip dengan bahasa mana pun saat ini (karena pada dasarnya C yang menjadi acuan sintaks mereka semua).

## 1. If / Else

Dungkus syarat-nya dengan kurung biasa dan kurung kurawal untuk area kodenya.

```c
#include <stdio.h>

int main() {
    int kkm = 75;
    int nilai;

    printf("Masukkan nilaimu: ");
    scanf("%d", &nilai);

    if (nilai >= 90) {
        printf("A (Sangat Bagus)\n");
    } else if (nilai >= kkm) {
        printf("B (Lulus)\n");
    } else {
        printf("C (Gagal, silahkan remedial!)\n");
    }

    return 0;
}
```

## 2. Looping (Perulangan)

### For Loop
Cocok apabila kita sudah tau akan ngulang berapa kali dengan pasti.

```c
#include <stdio.h>

int main() {
    // Pada standar C lawas, variabel i kadang harus dideklarasikan diluar for. 
    // Tapi di C modern bisa langsung int i=1;
    for (int i = 1; i <= 5; i++) {
        printf("Baris cetakan ke-%d\n", i);
    }
    return 0;
}
```

### While Loop
Cocok jika kamu tidak tahu pasti batas perulangannya, melainkan menunggui suatu kondisi berubah/ditolak.

```c
#include <stdio.h>

int main() {
    int uang = 5000;
    int tebusan = 2000;

    while(uang >= tebusan) {
        printf("Sisa uang: Rp%d. Bisa jajan lagi!\n", uang);
        uang = uang - tebusan; // uang berkurang
    }
    
    printf("Uang habis/kurang buat jajan. (Sisa: %d)\n", uang);

    return 0;
}
```

---
[⬅️ Sebelumnya: Dasar-Dasar](../01-Dasar-Dasar/README.md) | [Lanjut ke Array dan String ➡️](../03-Array-dan-String/README.md) | [🏠 Daftar Isi](../README.md)
