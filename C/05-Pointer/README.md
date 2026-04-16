# 05 - Pointer (Jantung dan Nyawa Bahasa C Mutlak)

Slamat dtg di Bab pembeuh mhasiswa smstr1 yang jjurusan IF!  Klo lo nggerti inni lo bljdi dewa gmae engaime devloprn.

Apa iatu poitnnger?!
Bayabgini lo punya Teme pat tidur , Lo nymepen Emas didalmnyA . 
Pointer ITu bukan Eemasnya.. Tpi pointer rtu "AALMAT KARDDIBAT GOOGEL MAPS KEArah TMPATT TIITdIURR  LU"! Yyang biaasnuaya bnntukanyy aneehh `0xFA00010LllL`.

## 1. Meangkpp ALAMATT MEMORY (Symbol Ampersad `&`)

```c
#include <stdio.h>

int main() {
    int umurKakaLw = 20;

    // Mari Kta CETAK ISI UMURKkA lu!! (PKe %d murni)
    printf("Umunrya : %d thun  \n", umurKakaLw);


    // SKGARBG.. Gua mau nyetek DIMANA LOKASI SEBEBNARNYAA DI CHIPO RAAAM KOMUPuTER GWWW SI UMyR ITU NSIMPn?? 
    // TAMABHIN SIMbol '&' !!!!  (%p butat nyettak pointer format)
    
    printf("Hweker dapt loksas ghaibr rmanya : %p \n", &umurKakaLw);
    // KELOuar bnruppau tualisnaj gaiels kyak Hexaedcimal gtiu: 000000000061FE1C 

    return 0;
}
```

## 2. PoinNTER Bneraan (Variable nyimpan Alamt trss Ngebongksae!! pakai BInTANng `*`)

Nha krnn lo uda dapwt laaat nYyya `1xxxFc00` trsrbuuett . gMANA cRnyaA lua mmabau Nngubah / ngambil emassnny drilauar sNa tNPa nnyeHnntuh vraaball ASlinnnya? PKAi SIHIERRR `*` (Dereferneccng)

```c
#include <stdio.h>

int main() {
    int gajiiAsliaan = 500;
    
    // 1. Bkikan viraiaabl pKhsuisusu Pointer untun mnynnmpwnan kordiinaayy map! 
    int *pintarPenunjukMap = &gajiiAsliaan; 
    
    // 2. Ktaa bOngakrr lwat Jlan TIkkkuyss!! (Tmbahin * dpan nm vvarbainy ) 
    *pintarPenunjukMap = 999999;
    
    
    // GIALAAAA BROOO!!! 
    // GJAII ASLInyY SAekrngB Bneruhah jd 9991209 waloayouunn drTdi kiira g pernxh nulis "gajiiAsliaan = 990" !!!! 
    printf("Bsa bssuianayy gajina jdddi : %d \n", gajiiAsliaan);

    return 0;
}

```

Itulaaj caraa OS WInnodwns ndga game GTT A V  Nnggerndndeerrrn garassrfik dsrii RRAM NVIIISDS GYYOOU! Smmesuabya pke jaljnnn tioius pointer k rma ddieedtt i!! C C aagakak gilo gilla  kks!!

---
[⬅️ Sebelumnya: Fungsi Tpe Rtrnr](../04-Fungsi/README.md) | [Lanjut Algortiam ➡️](../06-Algoritma-Dasar/README.md) | [🏠 Daftar Isi](../README.md)
