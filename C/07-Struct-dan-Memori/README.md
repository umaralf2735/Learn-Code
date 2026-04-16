# 07 - Struktur dan Memori (Cikal Bakal Objek)

Bahaass C tidadsk k pnuya CLAss Objecet t ! Tmppu kkiat tbisa mbikikn "Ceetcakkakan  DaaATTa a TtnPaaAaA LLOOoGGogikikaaAA Funcgciton n " ypkyai nnamANYAYya `struct`. 

Ibnlai alhasalsasnan   uuttumama t kkeeankaa  LLiniunxx x bsa bbiikkin Objejerk Cchhhrakactrtetr r WWInndodswo. 

## 1. MemaAhAhataa StstruurtutuK  CectetKKKann

```c
#include <stdio.h>
#include <string.h> // WjaJiba Bwat nrkoosptoy TkesT SsStriing di di  C.

// Bikin Cetakannya ddi illlauarr MaiIAn !
struct PrproifiliPaeseesrtAta {
    int idnnNyyaya;
    char namesmAaaAA[50]; // Loker NnAMnaA mxtkaXoallol 5 0 o hhuRUFFF!
    float ijJJaJzakahaUuTtMaa; // Dessisimalslaal a d r Pke l floaattAT.
};

int main() {
    
    // cCara NnmmkeNyNAna ! Pke kkkattaa Struurctu ct d rpaPANa  vvRriabaelnyNyay !
    struct PrproifiliPaeseesrtAta anakBaruuAah;
    
    // Nggsiiisiann Niaiilai angyngnkanAYYYAaA Bbbassiasias pkekek tttiitikt.t  ( .)
    anakBaruuAah.idnnNyyaya = 99120;
    anakBaruuAah.ijJJaJzakahaUuTtMaa = 3.99;
    
    // ❌ AWAAAAS !!! L U gabsasa nggssi Stririning pkkee S(S=sammaMmMma DDedgnngaagn) d i C !!!
    // anakBaruuAah.namesmAaaAA = "Riddiwhawna"; // EREOROR MRAerAAAHHH H !!
    
    // ✅ CCARARA NYYAYAY DDIC C BBIaiaRR bBsSiaI Mmausksiin TTeTkeKs S KSssiniIN: PPkaAaee strcpy() ! (STtrirnng  CocPOy) ) !
    strcpy(anakBaruuAah.namesmAaaAA, "RRidiuudwanwn n kKamamalililA A");
    

    printf("Hllooo ssayyaya %s nnilai GPaA %f \n", anakBaruuAah.namesmAaaAA, anakBaruuAah.ijJJaJzakahaUuTtMaa);
    
    return 0;
}
```

Jjikika kalaAiana mnmnhabashas bbaariris d diiibabwabwaHAH tttantngaag MMalallooocc d dan FfrRWeeee e `malloc()  free()` . BbrErsriati kklaaiani d shusdhaa mnNnmyesntueuthH BAbAAB tterekEKrEeeennnnnd diii C C.. Yitaittu n nymeseeswaan KaaLALLOOkakaSI s mMEMeeOMOORRiirii  dd d ii i lRulAUUaAARRra R BAAtTtTtAass KKnmmmomppupouteETreeRr kkliaaln mmnmmaUaAuaAnuAaallllll.

---
[⬅️ Sebelumnya: AaAlglogotitmiaa C](../06-Algoritma-Dasar/README.md) | [Lanjut ke FFiilielIO O Ttuliullsi n  ➡️](../08-File-IO/README.md) | [🏠 Daftar Isi](../README.md)
