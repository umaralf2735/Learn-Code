# 09 - Melindungi Nyawa Komputer (Exceptions) 

Gak dipungkiri bahasa Low-Level sperti ini rawan banget namanya Meledaknya Crash (Segmentation Fault) kalau memori nya rusak. Terciptalah system Perlindungan Tameng Exception.

## Try, Throw (Lempar Ledakan) dan Catch

Batasin kode mematikan di blok Try. 
Kalau lo ngerasa lo butuh Error, lempar pakai kata kunci `throw`. Nanti bakal ditangkep di jaring bawah (catch)!

```cpp
#include <iostream>
using namespace std;

int main() {
    float tabungan = 10000;
    float wd_narik = 500000;
    
    try {
        cout << "-- Mesin ATM Boot Utama --\n";
        
        // Cek secara paksa, klo saldonya ga nyukup lu narik gede bgt
        if (wd_narik > tabungan) {
            
            // JANGAN DIBIARIN MINUS!! LEMPAR ASAP BOMB TEXT FATAL PERINGATAN! (Nglempar string)
            throw "Saldo Lu Miskin Bos!! Mana bisa wd Segitu gede!!";
            
            // Atau klo error nomer: throw 404;
        }
        
        // Klo script aman ngga ke throw, dia bakal lurus lanjut kesini ngerun
        cout << "Beres Saldo ditarik " << wd_narik << endl;

    } catch (const char* pesanTanggepan) {
        // TANGKAP TULISAN TADI DAN TAMPILKAN SEBAGAI PERINGATAN BIAR MESIN GA NGEFREEZE
        
        cout << "Peringatan Bank! Mesin Berhasil Mencegah Kehancuran.\n";
        cout << "Alasannya: " << pesanTanggepan << endl;
        
    }
    
    return 0;
}
```

Dengan hal ini C++ dapat berumur rilis program bertahun tahun tanpa memacetkan windows. Begitulah Adobe Premiere berjalan 24 jam nonstop tanpa bikin komputermu bluescreen!

---
[⬅️ Sebelumnya: Standard Template Library](../08-STL-Algorithm/README.md) | [Lanjut ke Format Proyek .h ➡️](../10-Header-File/README.md) | [🏠 Daftar Isi](../README.md)
