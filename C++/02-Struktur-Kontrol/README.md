# 02 - Konstruksi Kaku Kontrol C++

Dalam C++, sintaks if-else dan looping murni menuruni kakek buyutnya (C dan Java). Tidak ada yang mengejutkan jika kamu telah fasih dalam blok dasar perulangan JS / PHP. Segala parameter tetap diapit didalam kurung `( )` dan body kurung kurawal `{ }`.

## 1. IF dan Else Logic Block

```cpp
#include <iostream>
using namespace std;

int main() {
    int darahKu = 0;
    
    if (darahKu > 50) {
        cout << "Gasss Serangg Boss!!\n";
    } else if (darahKu > 0) {
        cout << "Waspada sekarat bro panggil medic!!\n";
    } else {
        cout << "YOU ARE DEAD!!\n"; 
    }
    
    return 0;
}
```

## 2. Looping For 3 Babak Klasik

Digunakan berulang untuk memutar hitungan logika matematika atau menelusuri array polosan lama.

```cpp
#include <iostream>
using namespace std;

int main() {
    
    // Putar index dari 1...
    for (int iter = 1; iter <= 5; iter++) {
        cout << "Menetaskan telor naga ke : " << iter << endl;
    }

    return 0;
}
```
---
[⬅️ Sebelumnya](../01-Dasar-Dasar/README.md) | [Lanjut ➡️](../03-Array-Vector/README.md) | [🏠 Daftar Isi](../README.md)
