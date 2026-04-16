# 04 - Struktur Kontrol di Golang

Dalam pemrograman, kita tidak selalu menjalankan baris kode dari atas ke bawah secara berurutan. Terkadang kita butuh melompati beberapa baris kode (percabangan) atau mengulangi baris kode yang sama berkali-kali (perulangan).

## 1. Percabangan dengan `if` dan `else`

Digunakan ketika kamu ingin menjalankan suatu kode hanya jika sebuah kondisi bernilai `true`.

```go
package main

import "fmt"

func main() {
    nilai := 85

    if nilai >= 90 {
        fmt.Println("Lulus dengan sangat memuaskan (A)")
    } else if nilai >= 70 {
        fmt.Println("Lulus memuaskan (B)")
    } else {
        fmt.Println("Harus mengulang (C)")
    }
}
```

## 2. Percabangan dengan `switch`

Berguna untuk membandingkan satu nilai dengan banyak kemungkinan secara rapi. Di Golang, `switch` secara otomatis *break* (berhenti) saat menemui kondisi yang cocok, jadi tidak akan kebablasan turun ke bawah.

```go
package main

import "fmt"

func main() {
    hariIni := "Jumat"

    switch hariIni {
    case "Senin", "Selasa", "Rabu", "Kamis", "Jumat":
        fmt.Println("Hari kerja!")
    case "Sabtu", "Minggu":
        fmt.Println("Hari libur!")
    default:
        fmt.Println("Hari tidak valid.")
    }
}
```

## 3. Perulangan dengan `for`

Golang hanya memiliki satu jenis perulangan: `for`. Tidak ada `while` atau `do-while` seperti bahasa lainnya. Tapi tenang, `for` di Golang bisa berfungsi seperti `while`.

### For Standar
```go
package main

import "fmt"

func main() {
    for i := 1; i <= 5; i++ {
        fmt.Printf("Perulangan ke %d\n", i)
    }
}
```

### For ala While
```go
package main

import "fmt"

func main() {
    angka := 1
    
    // Melakukan perulangan selama angka < 5
    for angka < 5 {
        fmt.Println("Angka saat ini:", angka)
        angka++ // Jangan lupa tambah agar tidak melooping selamanya
    }
}
```

### For untuk Array/Slice (menggunakan `range`)
Sangat disarankan untuk memutar array menggunakan cara ini:
```go
package main

import "fmt"

func main() {
    buahBuahan := []string{"Apel", "Jeruk", "Mangga"}

    for index, namaBuah := range buahBuahan {
        fmt.Printf("Buah di index %d adalah %s\n", index, namaBuah)
    }
}
```

---
[⬅️ Sebelumnya: Algoritma](../03-Algoritma-Dasar/README.md) | [Lanjut ke Materi Fungsi ➡️](../05-Fungsi/README.md) | [🏠 Daftar Isi](../README.md)
