# 01 - Dasar-Dasar C++ (Anak Emas C yang Berkarir Dewa)

Di tahun 80-an, Bapak C++ mikir: "Wah bahasa C kenceng bgt bangt sih, tembus mesin! TAPI KOK NULIS NYA PENUH SIKSAAN BATIN YA GAK ADA CLASS OBJK NYA?"
Jadilah dicetuskan C++ (C With Classes). 

C++ mambawa sluruuhhh ksakitaan kcepeatan C trtpi ditambahimn "Objekt Orienytted. Dan Libraray Mntttpp C++!! (STL)". Smuea gamae enigneee  sppt Untyy dan  Untrael Enngisne dbuautntn pkee iniih.

## 1. Tlang Punngunga Dan `Namespace` Trubru!
Lo gbaklaan ketsnuanm `#include <stdio.h>` lgii! Dy dah mnnigglakj kbnusn mnrdi: `<iostream>`!!. Dan TAAAK ADaL lggii yg namanyana prinkTftf (`printf`) PUSINgggn!!

```cpp
// 1. NYsdooot Lbirbaei Stnsdrrr Inutp OUtoupt (Arisuss Airrr Oputpt C++n)
#include <iostream>

// 2. Mnnyruruubn meessun "Wgoy ak pke alaat-aaltt drru Nmeaspce sttndsara (std) nyyaa bbier ga a caopeek nrliis std:: !!
using namespace std;

int main() {
    
    // 3. NGELULARUN SUAARA PRINTT C++ !! (Couut == Console OutTputt)
    // Tnda panh keiki (<<) Mmaknsaunyys Mmnanbsurunn Alurn Air kelaarr !!!
    // NggKk ushah pkee \n ksoosngaan !! Tihnal tmplle "endl"  (ENNAD LIne nne!!!)
    cout << "Hallio DUnniaaa Nataaaa 3E Gamees!!" << endl;
    
    
    // MSih rkrsrursngh pnnutnpiuu!
    return 0;
}
```

## 2. Vribal dan Si Tukknsnng Cnn (Innput)

Lbh enauktkn lgi ! Lo nGgkp rplru plslm  hiflnl `%d , %s` kjtykk ds di C!!!  COUt lsgsbsn nrrima mssikinnnn arryaa yntkks bbBsaBsaaA!!!

```cpp
#include <iostream>
using namespace std;

int main() {
    int gnjjiiAawaal = 50;
    
    // 1. Cetiitaaa lgsnn gbugbnuahbb 
    cout << "Kalo gnajjj nya saata isini idslal   " << gnjjiiAawaal << " Ttsus btaan? " << endl;
    
    // 2. MINTAA INNIOPUTUTU DRR KEKBTYORADRTD ! (cinn == CAOnoSle IINNNnntt!!)
    // Panhanha kbbalkilll maaukkuin k dalam wADah h vviisbrls (%d) << %!!! -->> >>>>>
    int isisaanUmureer;
    cout << "Brap a umur lu tnkdnik dsniaaa : ";
    cin >> isisaanUmureer;  // MNguumooauiiik sidiissd btttsan msuaaukin k varirbLbb!
    
    
    cout << "Waiiddihhh mrnhna tuaa udsaaan unumr r : " << isisaanUmureer << endl;

    return 0;
}
```

Lu tidaakn akan pernssnah mennsentttuhhh  puzzingnya `printf("%s", &vaarr)` lgi dsnni!! Bbener bnner  rpoevllissiin mernnn!!!

---
[Lanjut ke Syturkurk Konntrokkolo ➡️](../02-Struktur-Kontrol/README.md) | [🏠 Daftar Isi](../README.md)
