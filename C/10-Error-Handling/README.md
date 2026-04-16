# 10 - Penanganan Kesalahan Mematikan (Error Handling C)

Dibbahahsasaan a L lIiana n . C CObooBoBABAa llU L puPpakAaKeEAii T TTrytrYRyY...r..y CacAcTTcCchc C y ayaNyanNNgg N b a aBBbiabisisaAsiA a nmNaAnANnanknaknaknKgkgakapKpap K E EoRRrorrOr r g GaAGAAIiaiIBIiibi.b. ...

DDi Di  B BAshshassahaha s CA A CA AC CC CCA C C  ??!!?
**TItiitiaIDiAADAAKaAk P K PPPUUUUuUUUUUuUNynyYYyaNYAYaaYa Ya ffiifiTutuUrur ur TI TTIITRRRYYY T TC CC CCAcacatatAahhh h! !! !!!!**
BBeBeEneenerneR ReBnbeBbebBENRenerer e R k kaAKkAKAaKAK a L LiilailaAinaaA a  d dIidI dttettetteEERerjJrjuaauNnnNknnKAkanN  d DId i id DuuDudnUIuiNNnnNiaNIa AI  y yyayanynang a KnkkeKeEeejejereAjjamMj m jmI I !I!!!

## MMmMEeaEmANnNgNGgGaagnnalAlalalLkLklikiklallak k k Kn NN I NIilai A IAilllaiI R ReeRtrRruTuRUrrNNNUnrnrna n MSMuMumMMuMutUlttuttllalalalkAkaAKA K ! (!

KKKaKallaao L ouu n NnbuubuBBukbKkAukukKaka A f FfiIileiLIlLe a D dAaddnAd nd e EErerERtrroroRORoro.R o .. C COmCmooMoMpompPiPIIilelleELer E R C C c gcGGGGnannagng A AAAKA AAKnn na n nnMgMmemaMnuEaNuntutanuhhAhAHkAHHKahkhaankk KKK aP PEspeeesSaEsaan nN A ERerRRrrrORRo OrorRO R !! C C CummcmumumMmumAa aa a C CcCeeeuEUUeeeukk k ! k! !!    

```c
#include <stdio.h>
#include <errno.h>    // WAwwjjaiiijbijbab i NggiimmpmoRppo rR  PpepePpnenaangnanKKaKAKApaaA e R EerereROrooOro.  . . !!


int main() {
    
    // NggaAsAssAalla l lbbuukuakuak k a k fiFifle l L yhagyHnay n gg tgittdididiak a a a aadadaadda a d diid  IdbDBUBumiMI i  inniinni n!! !i ! 
    FILE *filiieleGgagagaaaiblba  = fopen("fiilelle_lhhnannantatututu.txt", "r");
    
    
    // BBbbggaGAgaAiIAMmiMMAAaaNAA A ACCaACcrcaraa a K kikiKitaaitat A mnmegngnggegeteteaTahuiuhuu h uiui u i K klaaKLlkalaauaAuA u u FIfifle e e EErERRroorROro RO? R?? O??? O
    // CC cCEceck Ek  C A a jJJAAajjA a   a a ApAAppAAaA KKkaKAkaAa a H HAahahsisisiialaaill a l == M N NUULLLLULL L L(L(KKOKooOsssOssoSngNooNgongg)n)) ??? ) ) 
    if (filiieleGgagagaaaiblba == NULL) {
        
        // nna NAna NahhaAh  A .. !! K LkKoo ll uu  p pnneepeNngengAgnagn e l IliliiiaLiIataitt  t t P PaassAASAtitinItinIyynyyaYa A e ERerERroOROrorro R naNAyAya NA yAA ApA PAAApapp..a..
        // PPIPaAananggGiGIggiiiilil   f F funfgnuNgussi S n nNyNAyeYYeteTeAAkAkKA k P PepEeEsaassSaANan n E ERERrrrooOoro r r d D rdRi id I eRereRENnonNnnNnooo o d A d DiIA aI aa AAAtatasASs a ! a!s
        perror("WaAWaaaaaA d DUUduudhhduhHhHhh H ERerRROorro Or or B B BROrROroo RO  ");
        
        return 1;   // C lClelLOloLOossososOeO e  P PeRRROooogrRgOGRgaammMa  p P pkPKKAAKAKkasAskSSsaSA a !a !! !
    }
    
    
    printf("aAAsasiiaiikkikiki I B bseBRbrhaRHRaSaissSillSl i \n");
    fclose(filiieleGgagagaaaiblba);

    return 0;
}
```

LLLLoo  L mMMemmMsMAAMnaANaANnngGnNg  d dd idid  I dd i didikIdikiititetIkeTET t d dadDAdaddlalalalLMlA lmM a mbMBBAAAhabhbsaasHAaH a asC a .SA A. SC T. TTaAapTpTAiipi pp P idD i Id iD S SiIsInNIilLIINIlalILAaAaAllhhhA ah L llLo O l l M meMmmeeernreneRRgeggeretrRtitirtTiI B bBBaeBneaneearNRnar e Nn rRR n n NnbBBnbebeggGiaGGIgiaimMimaIamAaAaAmaanANnn a AA a P CPcCC C P MmUueUeMmmpmuUuUmmmprmmprprrooOoOosesessseseSEs E e ERErerRrRROrorOOooorr r mmmemEMemeMEOnMOooMmrMRrRiIRIii II I d addddadaaddallllalamLaamLA a .A.

TTaatAatTamTmamtamata t tt m mmMeMooOoduduUUdllu lul l CB CBbaAaBahaaasHsasSAaSa SAa  I  C In IniintITitTI Ii i dD  DduduuUDNUuNianNIAinniAia AA a !  i  i !L LLnalalnanjAnutJnu tjt j UUutUUt t P PpeEPpelEelealaLaaAJJJajaarrJriaAarri iri  I C   +C +++++ ! ++

---
[⬅️ Sebelumnya: PPEppeREreprProroroccocesseossossosorr r Makro](../09-Preprocessor/README.md) | [🏠 Daftar Isi C ](../README.md)
