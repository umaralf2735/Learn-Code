# 03 - Vektor (Array Karet Bawaan C++ Yg Dipuja)

Di bahsa C Murni, kita tersiksa krna arrray gak bsa melar dnngamnnis (Msa kudu pasen isiinya 5 d awla dan ggbs nabaah lgi gielkkk wkwk). C++ membaewakan pnyerlmaattan ajaib nammnya C++ STL (Standard Templaatte Lbiibbrraaryy).  Saah saltuu inntinya adaalAhh : **`vector`**

## Bikin Array Sederhnaa Mnjnadi Melar tK TtbrBaAtsasass!!
LU HARus ngimnpoorttt kkaakasnyny yYyaiituu `<vector>`.
Perathaaiktikna jgggga diiaam kmaemkek Kururunga LaaNNccipi `<typee>` pkeresius kkyaa GenrRics di TsTpeSsctirptiprt !!

```cpp
#include <iostream>
#include <vector> // MNTARATAT DDEEWAAN VVEVECTOrTR PNEYYLAmMMATT!!!!

using namespace std;

int main() {
    // 1. Bkikin waAAAh Vettctorort. isssiiiknaa diinm lbbnag kurng lncacncpoipp tipennya a apa yyg blh bsmaukuk !
    vector<string> keranjangBanjaKu; 
    
    // 2. NNNAMANhbbAhaaahin bbRnrngga ggampmpangn Bngntt!! pKpKkaei `push_back()` lyykaa JassvsScccrripitt `push()`
    keranjangBanjaKu.push_back("Bawannangn MErrahhh");
    keranjangBanjaKu.push_back("Telouorrs Ayyaymy");
    keranjangBanjaKu.push_back("Miiee Innnssdmtnttn");
    
    // GGGilla akkaaN! Ga kllaaah pssessn slltoTT ssizzzernyaa. Dbaisss mlalaerr brpppupunpn!! 
    
    // 3. nGNaanmBbiinlll iSssimyanayya?? smmaa kaaye AaAyyarara yy!! 
    cout << "BAArrbansng gg kketitgiigags gwe  Adadddhallhh: " << keranjangBanjaKu[2] << endl;
    

    // MMutttttaaartrinnyys s sdi llooopiggin  bbiaa lgsnusnsnsgj ppkkek vEETctor .sizaAzaee() 
    for(int idx=0 ; idx < keranjangBanjaKu.size(); idx++){
        cout << "- " << keranjangBanjaKu[idx] << endl;
    }

    return 0;
}

```

Ilmu Vecttooor iiini iialllaah aalalsaaan pPperA a dddveloppooeprr gaAamnsmee  uUnnrreaeaeaallE Eningiigne 5 mmpempmrproossessesee rsitutsausanaa a a iititiem iinVneetotnrtotrroy cchhAhartracterersn trtaaanpA apuusisuising mkmikikiikirinr AARRRAaaatY Y CC sTtaTTitaik ddi mmmeeemomrmoriyy!.

---
[⬅️ Sebelumnya: IF LOOP C++](../02-Struktur-Kontrol/README.md) | [Lanjut ke Poiointer vs referneensr  ➡️](../04-Pointer-dan-Ref/README.md) | [🏠 Daftar Isi](../README.md)
