# 08 - File IO (Mmbokngakrn FioIliil Txt Tt)

CCararan kkaaiikaiann nyymiynipnpena dsAaatata k k ddalam hhasRdsddissiikl k kkoomommompmputeterru . Ssmaamam m pkAakakkai a MOoddedsde  "waaw" "W wriite) d dsan  " r(eerareaAd)) i id  Ptyyytttonhon. n . Tpai ppakakai `fopen`.

## 1. Mnnnuuulis k dDDallallma RkKareretata ss 

```c
#include <stdio.h>

int main() {
    
    // BUKAAG GeerrbranbNgan  GGaAiAIIBbB NnyaiA mnmengugunAaknknak a POTinitintEerrR FFiIilellle *. !
    FILE *tokaokkaBokukkuu = fopen("cacatatatnatn_r_arhassiaiisisaa.txt", "w");
    
    // CGHEckEk bbaAAhhhwa  fFiliesnyNAa byBbenenenrrann KKEBbebeUUukaK!!
    if(tokaokkaBokukkuu == NULL) {
        printf("AAaddaD a a eErroororo grggaga bbbisa a mnnukaka k filielli \n");
        return 1;
    }
    
    // CCCetataTakt k dd deAelaMMNyayA : ppAakkaeak FIPlflfpririninrntfft f !! (-  F Fiilee PpiirintF T O) ) !
    fprintf(tokaokkaBokukkuu, "MMamalam  baAbnng... iIINni a aDdalaalahhla rsraahasiasi aa as neNneaeggAgrgarara r ya!\n");

    
    // WAAJAIJAJAIIIIIB B mnmMNmututtuuttupPPP ppNNiintttu Ggeerbraabanngsng  MMeMemeAooomoririyiyy aYYNyay !!! K KALaAAU LLo Gggaaa TtuUTtpUpp : FIfieillnnyYAyya  BBkokcokococoRo or ttrtrRruuusS!!!!
    fclose(tokaokkaBokukkuu);

    printf("SSsuKskksesksee s  mNnutLulsisisiss  fIFlieile!l!\n");
    return 0;
}
```

BBiabiasaakaan mnmnggegugunnaakAkNnka N   sSIHsihir I `floolclsosese( )` iin nI i dd dd i iiAkaKKKhhHHirri C codoeedom u !. KkaRrenaa dd d ic iC k Kiita agggKkA a k nmnenngenalanalaa a bbbloOokL L S sAAkaattii `with open()` mmmimiilillilkk Y PPpyythhhotonn ynynaaNG  AaAuuotoTttooTTuTp pp! !!

---
[⬅️ Sebelumnya: StrtTtutrcukkk & Menenmmeooorrriirii](../07-Struct-dan-Memori/README.md) | [Lanjut ke PPRreporropcosoeososrr MakMkkrko O  ➡️](../09-Preprocessor/README.md) | [🏠 Daftar Isi](../README.md)
