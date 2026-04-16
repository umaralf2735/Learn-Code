# 07 - Struct dan Method di Golang

Bahasa pemrograman modern lainnya punya yang namanya *Class* untuk menyusun data atau membuat OOP (Object-Oriented Programming). Golang punya versinya sendiri yang lebih simpel bernama **Struct** dan **Method**.

## 1. Struct

Struct (struktur) adalah gabungan dari beberapa tipe data yang berbeda, dibungkus menjadi 1 tipe data baru. Anggaplah kita ingin menyimpan data orang.

```go
package main

import "fmt"

// Mendefinisikan struct 'Mahasiswa'
type Mahasiswa struct {
    Nama    string
    Umur    int
    Jurusan string
}

func main() {
    // Membuat variabel tipe struct
    mhs1 := Mahasiswa{
        Nama:    "Dimas",
        Umur:    21,
        Jurusan: "Informatika",
    }
    
    // Mengakses bidang data dengan tanda titik (dot)
    fmt.Println("Nama Mahasiswa:", mhs1.Nama)
    fmt.Println("Umur:", mhs1.Umur)
}
```

## 2. Method

Method itu cuma sebuah fungsinya yang menempel pada sebuah tipe (termasuk menempel pada Struct!). Method adalah cara kita ngasih "perilaku" pada suatu data.

Daripada kita membuat `sapa(mhs Mahasiswa)`, lebih rapi jika fungsi itu "punyanya" Mahasiswa.

```go
package main

import "fmt"

type Kucing struct {
    Nama  string
    Suara string
}

// Ini method! Ada diletakkan Kucing sebelum nama fungsi
func (k Kucing) Bersuara() string {
    return k.Nama + " bilang: " + k.Suara
}

func main() {
    peliharaanKu := Kucing{
        Nama:  "Momo",
        Suara: "Miaaawwww",
    }
    
    // Cara memanggil method:
    fmt.Println(peliharaanKu.Bersuara())
}
```

### Tips
Jika dalam method kamu **mengubah** data didalam struct tersebut, kamu harus memakai Pointer pada struct-nya seperti ini:
`func (k *Kucing) GantiNama(namaBaru string) { ... }` . 
(Karena jika tidak, kalian hanya mengubah nama di obyek tiruan!)

---
[⬅️ Sebelumnya: Pointer](../06-Pointer/README.md) | [Lanjut ke Materi Goroutine ➡️](../08-Goroutine-dan-Channel/README.md) | [🏠 Daftar Isi](../README.md)
