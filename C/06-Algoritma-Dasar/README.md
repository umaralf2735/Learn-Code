# 06 - Algoritma Dasar (Manual Murni)

Di Javascript kita disuguhkan fasilitas instan nan mewah pakai `.sort` kelar 1 baris. Sayang seribu sayang, C dibentuk tidak memanjakan siapapun. Tidak ada perintah sihir (kecuali library rumit). Membangun Logika `Bubble Sort` adalah hal yang asik!

Sangat sering diujian algoritma Universitas ditanyain ini!

## Sorting Data dari Kecil ke Besar

Inti dari menyusun benda adalah memeriksa anak tetangga satu posisinya, kalau dia lebih besar, maka Gunting dan Tempel (Swap)!

```c
#include <stdio.h>

int main() {
    // Bayangkan array acak
    int balok[] = {50, 20, 10, 80, 40};
    
    // Hitungan rahasia (N) mencari banyak slot Array karena C orangnya pelupa!
    int n = sizeof(balok) / sizeof(balok[0]); 

    // Bubble Sort Murni Ala C !
    // Ulangi selama masih ada item
    for (int kiri_pol = 0; kiri_pol < n - 1; kiri_pol++) {
        
        // Cek tiap jejeran sebelahnya perlahan-lahan
        for (int jejer = 0; jejer < n - kiri_pol - 1; jejer++) {
            
            // JIKA balok yg sekarang ini nilainya KEGEDEAN dari tetangga kirinya..
            if (balok[jejer] > balok[jejer+1]) {
                
                // --- PROSES SWAP MENGUNGSIKAN CANGKIR ---
                int cangkir_gelas = balok[jejer];   // amankan teh e ke botol
                balok[jejer] = balok[jejer + 1];    // siram isi kopi tetangga ke teh
                balok[jejer + 1] = cangkir_gelas;   // seduh balik balok nya
                
            }
        }
    }

    // Mencetaknya harus pakai Looping pula, tidak bisa diprint langsung kotak!
    printf("Sudah Urut Bos!\n");
    for (int d = 0; d < n; d++){
        printf("%d ", balok[d]);
    }
    printf("\n");

    return 0;
}
```

Jika ini dilarikan di C, kecepatannya ngalahin Java loh bro! Murni logika murni hardware!

---
[⬅️ Sebelumnya: Pointer](../05-Pointer/README.md) | [Lanjut ke Manajemen Memori ➡️](../07-Struct-dan-Memori/README.md) | [🏠 Daftar Isi](../README.md)
