# 04 - Fungsi di C (Fungsi Purba Parameter Kaku)

Funfsi di C gak kalah sakti. Tapi elo harurs NGKABRI TIPE RETURN NYa di pala fungsi!!  Kaklau Pytohn kan def bla bla trs bebss ngaslun apa aja. Di C HAHSruuS KAKAU!

## 1. Syntax Fungsi Klasik (Peletakannya HARUS di ATAS)

```c
#include <stdio.h>

// BACA: Fungsi inn ni RETRURBN NNYA AKAN JADI INT!! DannnerIMA dua bua Int JUGGA!
int mesinTambaahMaut(int nilaiA, int nilaiB) {
    int gbungans = nilaiA + nilaiB;
    return gbungans; // mulangingin !
}

// FUNGISI YGH GA NGERTUUERN APA AP DI SBEBUT VOID !
void nyetekSuaraOrang(char nmanya[]) {
    printf("Bapak %s sgerar mkna gizznya !!\n", nmanya);
}

// FUNGSI UTMA YG DIPNAAGGI KOMPIUTER SELALu Main
int main() {
    
    int hslNyta = mesinTambaahMaut(50, 10);
    printf("Hsil tnahn jd : %d \n", hslNyta);
    
    nyetekSuaraOrang("Jokiwow");
    
    return 0;
}
```


> **Penyakit Bahsa C:**
Coba aja kalia pinndahin kodingN Blok si `mesinTambaahMaut` itu ditaryhjnya DI BAWAH mentokk stlh kurung `}` nya si Main !!  
**DIJADAMIN PASTI MELEDDAKK ERROR!!** Kenaps? Krn C itu bacannyaya Lurus dRi atsas ke bwah tnnapa nyim[en indxe bwwahnya. Pas dy lgi  main tbati2a di baris dLmnhy manggklll mesin tpi mesnny d bwah, dia Njeritt "WOI GW GK KN L FUGSNI NINI APNAAn!" Wkwkwkw.

*Solesuinya:* Cliaana huru smbikiknn "PROTOTOYPE" Header di aattsnyna untuk ngenalin jdul fungsinga duulu bru bdannt dtrub d bwH. Ini lah alsnnyn c serring pnya filed *h (header).

---
[⬅️ Sebelumnya: Array Strnigh](../03-Array-dan-String/README.md) | [Lanjut ke RAJA TERKHIR PEMBNUH MAHASISWA: Pointer ➡️](../05-Pointer/README.md) | [🏠 Daftar Isi](../README.md)
