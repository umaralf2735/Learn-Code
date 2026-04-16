# 08 - File I/O di C++

Daripada pakai syntax rumit bahasa C, C++ menggunakan I/O Stream layaknya `cout` dan `cin` bernama `fstream`.

```cpp
#include <iostream>
#include <fstream>
using namespace std;

int main() {
    // Tulis file
    ofstream fileTulis("data.txt");
    fileTulis << "Halo dari C++ murni" << endl;
    fileTulis.close();
    
    // Baca file
    ifstream fileBaca("data.txt");
    string isi;
    while(getline(fileBaca, isi)) {
        cout << "Isi: " << isi << endl;
    }
    fileBaca.close();
    
    return 0;
}
```
---
[⬅️ Sebelumnya](../07-Memory-dan-Pointers/README.md) | [Lanjut ➡️](../09-Template-Generics/README.md) | [🏠 Daftar Isi](../README.md)
