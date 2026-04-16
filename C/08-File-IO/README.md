# 08 - File Input / Output (Menulis Teks Permanen)

Program kalian selama ini nyetak di layar terminal kan? Sekali terminalnya di-Close `X`, angkanya hilang dong memori mereset dari nol. 

Supaya nyimpen permanen, kita harus menulis langsung ke Harddisk dengan membongkar I/O File System!

## Buka Tutup Pintu Gerbang `.txt`

```c
#include <stdio.h>
#include <stdlib.h>

int main() {
    
    // 1. BUANG POINTER KE FILE. 
    // "w" artinya (Write) atau Tulis. Hati-hati ini bakal nimpa data lama.
    // Jika ganti "a" (Append), maka nulis baris baru dari bawah teks lama.
    FILE *dokumen_saya = fopen("catatan_rahasia.txt", "w");
    
    // Selalu cek takutnya harddisk kepenuhan atau kita bkn admin
    if(dokumen_saya == NULL) {
        printf("Aduh Bos! File gabisa dibuka/dibikin!\n");
        return 1; // Keluar kode Error = 1
    }
    
    // 2. MENCETAK TULISAN SEPERTI BIASA MENGGUNAKAN 'f' printf
    fprintf(dokumen_saya, "Halo! Ini baris ke-%d yang aku tulis dari code C murni.\n", 1);
    fprintf(dokumen_saya, "Dan ini di save lho ke Hardiskmu.");
    
    // 3. JANGAN PERNAH LUPA TUTUP! JIKA TIDAK AKAN BOCOR!
    fclose(dokumen_saya);
    
    printf("Proses cetak tiket PDF / Teks selesai lapor komandan..\n");

    return 0;
}
```

Sekarang coba buka folder kalian. Voila, akan ada file `.txt` rahasia yang tercetak disana tanpa pernah kita buat klik kanan manual!!

---
[⬅️ Sebelumnya: Struct & Memori](../07-Struct-dan-Memori/README.md) | [Lanjut ke Preprocessor ➡️](../09-Preprocessor/README.md) | [🏠 Daftar Isi](../README.md)
