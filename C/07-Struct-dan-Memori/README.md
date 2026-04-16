# 07 - Struct & Memori Dinamis (Peminjaman RAM OS)

Kelemahan terbesar *Array* biasa yang tadi kita pelajari adalah ukurannya yang kaku permanen dan tak bisa melar/mengecil (Bikin Boros!). Sedangkan Struct sangat mirip dengan OOP Golang.

## 1. Struct (Kumpulan Variabel Campuran)

```c
#include <stdio.h>
#include <string.h>

// Membangun Map blueprint milik Siswa
struct Siswa {
    char nama[50];
    int absen;
    float rata_rata;
};

int main() {
    // Membuat spesimen siswa benerannya
    struct Siswa budi;

    // Manipulasi Struct nya ! (Ingat char pake strcpy kalau nimpa)
    strcpy(budi.nama, "Budi Rahardjo");
    budi.absen = 12;
    budi.rata_rata = 85.5;

    printf("Nama %s di nomor %d dpt skor %f\n", budi.nama, budi.absen, budi.rata_rata);

    return 0;
}
```

## 2. Kebebasan Mutlak: Malloc dan Free (Dynamic Memory)

Ajaib, kalau kita ingin membuat array yang "Besarnya ngikutin Tuntutan User/Kondisional", kita bisa mencuri slot kosong Windows sementara menggunakan `malloc` (Memory Allocation).

```c
#include <stdio.h>
#include <stdlib.h> // Library Wajib Malloc dan Free!

int main() {
    int tuntutan;
    printf("Berapa panjang lintasan lari? ");
    scanf("%d", &tuntutan);

    // Minta memori sebesar TUNTUTAN dikali Berat Integer (4 bytes) 
    // OS nitipin ini kesebuah Pointer (*lintasan).
    int *lintasan_dinamis = (int*) malloc(tuntutan * sizeof(int));
    
    // Periksa dulu kali aja PC kita kepenuhan memori
    if (lintasan_dinamis == NULL) {
        printf("RAM BOCOR HABIS DITOLAK OS!\n");
        return 1;
    }

    // Ayo isi memorinya seperti array biasa !
    for (int w = 0; w < tuntutan; w++) {
        lintasan_dinamis[w] = (w + 1) * 10;
        printf("Isi Slot [%d] diijinkan: %d\n", w, lintasan_dinamis[w]);
    }

    // RULES MUTLAK MEMATIKAN BAHASA C:
    // UANG YANG DIPINJAM HARUS DIKEMBALIKAN! 
    // JIKA LUPA MENGEMBALIKAN MALLOC, RAM KOMPUTERMU AKAN BOCOR DAN MELEDAK BLUE SCREEN (Memory Leak).
    free(lintasan_dinamis);

    return 0;
}
```

Seram kan? Tapi itulah mengapa Sistem Operasi Windows dan Kernel Linux ditulis dengan bahasa C/C++. Karena mereka bisa ngobrol langsung dengan RAM perangkat kerasyang dipakainya dengan kecepatan mengerikan!

---
[⬅️ Sebelumnya: Algoritma Manual](../06-Algoritma-Dasar/README.md) | [🏠 Daftar Isi Utama](../README.md)
