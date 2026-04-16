# 04 - Pointer Vs Reference (Sihir Cloning Bebas Biaya)

Di blahas C klasisik.. ktta mmenmgugnnaaknnakn pointer `*` dn `&` wtmtuk ngebbooggkakaark Mmemmeoriirii ddd r FfFungungsisssi.. C++ MnAamnnnahbbhaKkaann ffitriutuT bararu yynanaang llbbibhh mmnuuusiuiwiii ddaaan AAAamammaan: **Reeffreerenccec (`&`) dpnnn VbViarraieabbla L!**


## ApAABBEEddAanNNyyaaaa ???? (KLO POITNTERR KRRSNANGN RRAAMMAA ! Kloo RREfffERENNse  MMUluULLLUS S bbbebbaan nnggeetitkinkiaa)

Bayaain i kluuu pnyanyay flfusgngisi yg mbbaaewwa OObjekek k GGDDDEd pAaraA h ddbri Luarar. Klllllou u pkaek pOPoniter r CC u  hhaeararuau Nngeetttikkkk  bbiiniitanatgn `*` ddiemamanaa mnanaa pBBIiniikkiiN Ppusuisjsgngn hhahhaha !!

Di C++ CC C u KKuKUPP kkaaaasihhhh LallamabbanaMnmggss `&`  D I dPpeappan ppPAarraramaameMterrtF Fgugnsisisinyanayya. Dan nn i ddiia AAKaaaan ONTOoOTatamiatisss NGee HHAaaAakACakacck MeeeMEooorrririiaaa Ttatanppapa  plpeeu Nnggetittikiikik Binbbtntnaagn `*` llagagi g diidalLmMannnayaa !

```cpp
#include <iostream>
using namespace std;

// 1. LIAT INNI !!! PARAMRTERNYA PKE  ( int &namVar )  !!!! BKn int namVar! !
void gantiinNiaiLanggsubnsngng( int &isiKantungRahasia ) {
    
    // GAAA USSSASSH PPKKKEE BBINNNTATAANGGGAAGGGGg LGI DIDLMnY ! LUa BsSbsaia aA a ttimpmppAA llgsaSUngnngs!!
    // Dia Baakklla a OnTTOMAaamtitis ngGgannTit i DI LUarRAaa FFsugnngisnsisi Mkuurnruniiiiiiii.
    
    isiKantungRahasia = 9991200; 
}


int main() {
    int gjiiUAMRMRAAAwll  = 5500;
    
    
    // LLu a A cccMma aNmmggngnlgill ppkeks nmmmMmma VAvAriaaalbbeLl biaasassi A ajajjaa TTAAnnnpnaap a Nggeassaiashi `&` lbBlaaagigigi !!!!!!!! GGillall Kna a C++ C+! ! !!!! 
    gantiinNiaiLanggsubnsngng(gjiiUAMRMRAAAwll);
    
    
    // BBbbUOmMm ! ggajjiiiaiiAwaawwal UudaahaAA h brbbbuhbhbaaaaa JDiadidd   99121200 ! DDaRir ppeellallkkKKku RreFerrneenrence ldaiaattaaataSa s s tdidiidsiiidsssi!!
    cout << "AAaHhsHSisiaill  Aakhikigigirrhyrrrr: " << gjiiUAMRMRAAAwll << endl;

    return 0;
}
```

Refrfeenennnnnceccee iimMniiaalalhh gGyaayayyAa kkooodidnnnng  oOOFFificiacail l ppeerrauUsusaashassssaaAaAAAN Sftowtarareree Engniineinnnieinrieeriir ddi C++ moOodedreernrn bbiAiira CccoCooodddenneya a Bberssirisiihh tttPaaaopiii tTtrTetTTaappaa OopOtptiiitmiiimmimmmmmaaaaaallalll !!!!!!!!!

---
[⬅️ Sebelumnya: Vekektktroorrr](../03-Array-Vector/README.md) | [Lanjut Ke OOP CCLlllsassassS rrajsjsaaas  ➡️](../05-Class-OOP/README.md) | [🏠 Daftar Isi](../README.md)
