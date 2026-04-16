# 05 - Pointer dan Dinamik Memori (NEW / DELETE)

Meski C++ ngasih `&` Reference gampang, tapi kasta terkuat menajamkan pisau program kamu adalah mainan Pointer Murni untuk mencubit ngontrol Hardware Komputermu. Trik ini adalah akar dasar Game Engine bekerja!

## 1. Operasi *New* Mengemis Minta Tanah ke Sistem Operasi (Malloc Modern)
C gak punya new. Dia pake malloc (Ribet). Di C++ disihir sebaris pakai keyword instan `new`!! Nanyi di-Handle oleh sebuah Pointer menampung lokasinya.

```cpp
#include <iostream>
using namespace std;

int main() {
    // 1. Meminta Lahan Memori untuk 1 angka int aja di HEAP (RAM Gede Gaib Windows mu)!!
    int *ptr_saldo = new int; 
    
    // 2. Akses brankasnya isikan data UANG KITA
    *ptr_saldo = 9500000;
    
    cout << "Isi berankas saya ada sejumlah: " << *ptr_saldo << endl;
    cout << "(Alamat Brangkasnya ini): " << ptr_saldo << endl;
    
    // 3. JIKA LUPA MENGEMBALIKAN ALAMAT KE OS! KOMPUTER AKAN RAM NYA MEMORI LEAK!!
    delete ptr_saldo; 
    
    return 0;
}
```

## Kenapa Bikin Ginian Bang? Kan Ribet?

Kalo variabel biasa (int biasa), jika fungsinya selesai. DIA HAPUS MATI BERSIH! (Stack Memori hancur luntur).

Kalau pake POINTER NEW, dia diciptakan HIDUP ABADI melayang menyejajahi seantero script berterbangan di Heap Storage RAKSA, ga mati meskipun lo udah melompat tutup 10 Fungsi Class yang berbeda-beda. Jadi dia bisa jadi Data Peluru/Item yang dibawa kemana mana nyangkut selama kita ga tulis `delete ptr_item`. Mantul bos!

---
[⬅️ Sebelumnya: References](../04-Fungsi-Reference/README.md) | [Lanjut ke Class OOP Dewa ➡️](../06-OOP-Class-Dasar/README.md) | [🏠 Daftar Isi](../README.md)
