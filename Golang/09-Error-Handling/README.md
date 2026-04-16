# 09 - Error Handling di Golang

Di bahasa lain biasanya menggunakan `try ... catch` untuk mengurung kode yang rawan error. Golang tidak melakukan itu. Golang memperlakukan `Error` selayaknya **nilai kembalian biasa** yang harus selalu kamu cek nilainya!

## 1. Menangkap Error

```go
package main

import (
    "errors"
    "fmt"
)

// Fungsi yang mungkin bisa gagal
func bagiAngka(a, b int) (int, error) {
    if b == 0 {
        return 0, errors.New("tidak bisa membagi dengan angka nol")
    }
    return a / b, nil
}

func main() {
    hasil, err := bagiAngka(10, 0)
    
    // Ini adalah pola PALING UMUM di Go. Selalu cek `if err != nil`
    if err != nil {
        fmt.Println("Waduh ada error:", err.Error())
        return // Menghentikan eksekusi kalau error
    }
    
    fmt.Println("Hasilnya adalah:", hasil)
}
```

## 2. Panic dan Recover

Kadang program benar-benar tak tertolong (fatal error). Kita bisa memanggil `panic()` untuk mematikan program secara paksa saat itu juga. `recover()` digunakan jika entah bagaimana kita ingin mencegah program kita tiba-tiba tertutup padahal masih bisa dimaafkan.

```go
package main

import "fmt"

func jalankanSistem() {
    // Fungsi defer akan SELALU dieksekusi tepat sebelum fungsingya selesai (atau ambyar)
    defer func() {
        pesanPanic := recover() // Coba tangkap kepanikan
        if pesanPanic != nil {
            fmt.Println("Sistem pulih dari crash! Penyebab:", pesanPanic)
        }
    }()

    fmt.Println("Memulai sistem...")
    panic("DATABASENYA TERHAPUS NIH!") // PROGRAM CRASH DISINI
    fmt.Println("Baris ini ngga bakal ke print") 
}

func main() {
    jalankanSistem()
    fmt.Println("Aplikasi utama masih aman berjalan berkat recover.")
}
```

Dengan menguasai pengecekan Error manual, program Go buatanmu akan terhindar dari *bocor* ataupun ngehang karena *crash* yang tidak disengaja.

---
[⬅️ Sebelumnya: Goroutines](../08-Goroutine-dan-Channel/README.md) | [Lanjut ke Go Modules ➡️](../10-Go-Modules/README.md) | [🏠 Daftar Isi](../README.md)
