# 03 - Ilusi "String" & Brutalnya Kapasitas Array C

Lu inget di Python lu bsa nambahin barang kedlem array Pake `append(Teks)` hngga mreka jd melar ?

DI BAHSA C.. **ITU MUSTAHIL TERJADI !!**

## 1. Array Kaku Murni (Batu Karang)

Saat lu mmsesan Array. Lu HAruS MUTLAK MASUKIN ANGKA SLOT PANJANG YANG LU MAU! Nggak bsia dinkbubah lg sisa umrn program mu.!

```c
#include <stdio.h>

int main() {
    // BIKIN KOTAK PENSIL ISISI 5 SLOT KOSONG! (Ga bkal bsa tmbah brng ks_6 !!!)
    int celenganNilai[5];

    celenganNilai[0] = 50;
    celenganNilai[1] = 90;

    // Cara Bca Isiya? HAarais pke Loop For manual !! 
    for(int i=0; i < 5; i++){
        // Wah tpe bwaah nya psti pnnuh angkaa ksoong/ 0 / hntu krn g ku dsisis niali tddi !
        printf("Slot ke %d adalh nlia : %d \n", i, celenganNilai[i]);
    }

    return 0;
}
```

## 2. Kenapa Gak Ada STring di C?

Krny nyiemopen Teks panjang sbnrny cm Mnyeimpana array dari HURUF!  Akhir dari stuab teks di C bakaL DI TEMPELIN TAMDA HANTU GAIB Yaitu Karakter Null `\0`. Buat nggasih tau RAM bwha ini "TEKS UDA MENTOK DISINI GANZ"!

```c
#include <stdio.h>

int main() {
    // Trik bikin Strring: (Bkinsaja arrat cnaracter !! Panjang slot ksosngk gpp bs dibca kmpileer sndiir!)
    char panggilnKu[] = "Si Jago Koding C";
    
    // Tapi gmn Klo lo mau ngubah namnnya?? LO GABISA NGETKI BGNI: panggilnKu = "Berubh!!"  
    // ITU BACAL ERROR PANNJG  MRAAAHH!! KRN lu ud mesen prmnent arrray string tsbut!!

    printf("Hwlo mas %s \n", panggilnKu);

    return 0;
}
```

Pusiung kann?? Sbenry ya emmgi inilah jeroa mnsin sebanarya dr CPU Intel kalian memprsoes RAM. Semua bgaaha lian sbnrny cmn Nutupiun krbuemnitan inin pke librsay!!  (Kecuiilu nnti lo belkjar c++ bru ad Sting Bnena!).

---
[⬅️ Sebelumnya: IF FOrr](../02-Struktur-Kontrol/README.md) | [Lanjut ke Tipe C Func ➡️](../04-Fungsi/README.md) | [🏠 Daftar Isi](../README.md)
