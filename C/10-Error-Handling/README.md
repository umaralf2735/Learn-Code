# 10 - Error Handling di C (Jalur Manual)

Di Rubymu ada `begin-rescue`, di JS ada `try-catch`. Nah, gimana dengan bahasa C?

**Pahit tapi fakta: DOSA TIDAK DIAMPUNI DI C.**
Tak ada "Try Catch" di pondasi C Vanilla (Itulah kenapa saudaranya diciptakan: C++). Di C, jika indeks array kamu kebablasan / memori RAM rusak, maka layarmu Auto *Segmentation Fault* alias Blue Screen!

TAPI, ada *Best Practice* tingkat internasional agar PC tidak hancur kok:
Gunakan Variabel Pengecekan **Global `errno` (Error Number)!!**

## Menangani Pesan Maut Dengan Elegan

Perintah perantara yang melanggar hukum, sebagian besarnya akan memberikan Output balikan berupa angka Minus (`-1`) atau `NULL`.

```c
#include <stdio.h>
#include <errno.h>    // PERPUSTAKAAN KHUSUS LIAT KODE ERROR DOSA
#include <string.h>   // MEMBUKA KODE DOSANYA JADI TEKS

int main() {
    // Kita menantang maut dengan mencoba membedel file yang KITA TAHU GAK ADA DISINI
    FILE *buku = fopen("file_gaib_yang_ga_akan_ada.txt", "r");
    
    // MENJEBAK ERROR MANUAL:
    if( buku == NULL ) { // Nah kan NULL dia
    
        // Jangan panik, program belum nge-freeze asal kita stop disini.
        int kode_dosa = errno; 
        
        printf("Astaga, Sistem terhenti kak!\n");
        // strerror adalah membongkar error global berdasar kode yang terekam
        printf("Pesan asli dari Sistem Operasi Kernel: %s \n", strerror(kode_dosa));
        
        // Output dari Strerror biasanya adalah: "No such file or directory"
        return 1;
    }
    
    fclose(buku);
    return 0;
}
```

Trik inilah yang dianut Go bertahun-tahun kemudian menjadikan C dan Go sangat identik pola manusianya. Kamu kini sudah siap membedah sistem operasi dunia memakai senjata penuh Bahasa C!

---
[⬅️ Sebelumnya: Preprocessor](../09-Preprocessor/README.md) | [🏠 Daftar Isi Utama](../README.md)
