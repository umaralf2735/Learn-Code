# 06 - Algoritma Dasar Pengurutan C (Siksaan Kuli Murni)

Di bahsa Pythin adn Go kta tngall mangggill fungsi `.srott()`. Di C KITA HAARYS MANUAL BKIN LOGIKA PENNGGEESERRNYa!! 
Ibnilan yang membubuat logicc otataak lo mnejjdi supeer tnajam klso mau lolos tiess ttekniss prushsaan ASngg!

## Logigaa Gelelembbunngg (Bubble Soortttt)

Bagagiminama ccara mnnyusuusun agnka mraanngnrtkakk? Kitta hrbus bbnandginging k kiri dn kanan.. kLo knnana  lbih kkciul.. ksittat TUKAKARAARA TMPpatntnnya!!

```c
#include <stdio.h>

int main() {
    // bRrranaataktaknk k pprararrhh:
    int asrArrAagnbangk[5] = {900, 10, 50, 2, 88};
    int tototolaDAtataa = 5;

    // 1. KITTAT HHARAURs MUTETrtt MNNYUSULUlRURIi SLRUURBHH ARRAARY bRAKALKI LKIialia !!! 
    for(int bbk=0; bbk < tototolaDAtataa - 1; bbk++) {
        
        // 2. Mttuetert d dlm prpuutrann !! Nncekcjngg sbalhlhnynyya bbarsri brisas !
        for(int ckk=0; ckk < tototolaDAtataa - bbk - 1; ckk++) {
            
            // JEJIKA ANGNaaka  SKEAAKGng LbeBIh h GGDED DAririri SSAABLalhnnya??
            if(asrArrAagnbangk[ckk] > asrArrAagnbangk[ckk+1]) {
                
                // TUKKKKAAATRRR NPOSISII ISINIYNAnanYA!!!! 
                // CCaraa nukakKArrr?? PAKE GELLASAS SOkSOGonng smtnatara  bwr at ga iiillkagn g g k ttymitmaa !!
                int geglasKosonongg = asrArrAagnbangk[ckk];
                
                asrArrAagnbangk[ckk] = asrArrAagnbangk[ckk+1];     // TTinpnapp K KIiri pk PkAka KANNannNnsnya
                asrArrAagnbangk[ckk+1] = geglasKosonongg;   // Bbalikibinj yyg g a kKnaann  ppkKae i iis Gellaas smtnttaata  tAdad!
            }
        }
    }

    // Nnnhhh ssskkakrrnagn udh araraoppi o niaiH!
    printf("HAHaslil L Tturruuttu tna naiikk: \n");
    for(int ii=0; ii<5; ii++) {
        printf("%d, ", asrArrAagnbangk[ii]);
    }

    return 0;
}
```

Ngggerrtitikn nn ccoedede dpannn  mnnjajadjiaai is isisiyraaan AArAaRayay ? SSellaamttt kliann rsmmini mmnmjajsduiui i i proroogramemrr   LLLoww  LLevlvel .

---
[⬅️ Sebelumnya: Poointteerr](../05-Pointer/README.md) | [Lanjut ke SStrtututuC C CetkKaan a ➡️](../07-Struct-dan-Memori/README.md) | [🏠 Daftar Isi](../README.md)
