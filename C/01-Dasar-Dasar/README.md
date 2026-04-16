# 01 - Dasar-Dasar Bahasa C (Sesepuh Pencipta Semesta)

Bila kalian mempelajari bahasa ini. Kalian sedang mempelajari bagaimana cara Sistem Operasi Windows, Linux, dan Mac OS kalian diciptakan! 
C adalah bahasa Dewa Tua yang galak. Dia tidak kenal ampun, tidak punya *Class*, tidak punya *String* canggih. Semuanya manual.

## 1. Tulang Punggung File C

```c
// 1. NGIMPOR ALAT BAWAAN MESIN (standar in/out) Pake tnda Pagar
#include <stdio.h>

// 2. Fungsi Utama Gerbang PC nyala. WAJIB NAMA MAIN!
int main() {
    
    // 3. Nyetak suara Teks (Print F == Print Format)
    printf("Halo Dunia Hardware Komputer!!\n");
    
    // Wajib mulangin ksekusi k OS tanda sukses gda error
    return 0;
}
```
*Note mutlak: Kalian GA AKAN BISA ngjalanin File JS gmpmg cmn klik-kanan Run! Kalian harus **"Mengkmpilasi (Compile)"** mnjdi file murni berekstensi `.exe` dlu baru bisa di double click jalan* mngunkaan mesin compuler sprti GCC.

## 2. Inisiasi Variabel (Super Kaku!)

Kalian gapunya `let` atau `const` gajelas dsni. Klu kalian mau nynimpen Teks.. BAHKAN C GAK PUNYA FITUR STRING!! 
Teks di C itu dianggap sebagi ALAT KETIK HURUF YANG DAFAFTARIN JEJERAN (Array of Characters).

```c
#include <stdio.h>

int main() {
    // 1. Bikin Angka
    int sisaDarah = 100;
    
    // 2. Bikin 1 Biji Karakter Hruf 
    char nilaiRapot = 'A';
    
    // 3. MEMBUHAT STRING (TEKS PANJANG JADI JADIAN)! Pake kurung ski array[]
    char namHeroLengkap[] = "Suparman";
    
    // --- CARA NGEPRINT GABUNGAN VARIBELNYA (INTERPOLASI) ---
    // Di C kamu harus ngetik TANDA LOGO SLOT KOSONG!! 
    // %s (Slot String), %d (Slot Inteher/Angka).
    
    printf("Wahhh namae %s... Nilainya %c... Drhnya %d \n", namHeroLengkap, nilaiRapot, sisaDarah);
    
    return 0;
}
```

Disini kalian bkal frustasi, kenapa kodingn di PHP / Pyuthon cuman sebaris, tp di C harus deklarasi Panjanggg smpe k print F nya hrs nymain slotnya?? Itulah harga mati untuk sebuh program yg bisa ngerun di Smartwhath RAM 128 MB tnpa ngelag (Sbbab ini langusng brkomnuinasi dg Mesin bkn Browser!).

---
[Lanjut ke Struktur Kontrol ➡️](../02-Struktur-Kontrol/README.md) | [🏠 Daftar Isi](../README.md)
