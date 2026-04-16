# 03 - Penyelamat Array Bawaan C (Vector!)

Tantangan di bahasa C adalah: Array nya `[5]` kaku permanen mampus gak bisa dilonggarin. Di C++, sang penemu meletakkan sistem sakti dalam Pustaka Standar-nya (STL).

Alat pengganti Array ini dipanggil *Vector*. (Persis plek ketiplek kayak `List<>` di C#).

## Bermain Vector Panjang Merenggang

Memerlukan tarikan include `<vector>` dari atap program!

```cpp
#include <iostream>
#include <vector>  // INI WAJIB KALO MAU MANGGIL KEKUATANNYA
using namespace std;

int main() {
    // 1. Mendeklarasikan Array Kosong yang tak terhingga! (Memakai Tipe Kurung Sihir < > )
    vector<int> kantongSkor;
    
    // 2. Menambahkan ke slot buntut (Seperti Push-nya Javascript arr.push!)
    kantongSkor.push_back(100);
    kantongSkor.push_back(50);
    kantongSkor.push_back(20);
    
    // 3. Menghapus yang paling BUNTUT
    kantongSkor.pop_back(); // Angka 20 mental kebuang dr memori!
    
    // 4. Kita lihat size brp yg sisa di dalem array?
    cout << "Jumlah isi loker ku: " << kantongSkor.size() << " Benda!" << endl;
    
    // 5. Bisa dipanggil secara biasa gaya Array C!
    cout << "Barang pertama sapa: " << kantongSkor[0] << endl;
    
    return 0;
}
```

Penyedia Array Vector inilah yang membuat orang beralih dari bahasa C biasa memigrasikan program berat nyari gampang ke C++ dalam semalam. Mengatur array gaib tanpa `malloc` manual. Mantap.

---
[⬅️ Sebelumnya: Struktur Kontrol](../02-Struktur-Kontrol/README.md) | [Lanjut ke C++ References ➡️](../04-Fungsi-Reference/README.md) | [🏠 Daftar Isi](../README.md)
