# 01 - Dasar-Dasar Golang

Selamat datang di langkah pertama belajar bahasa pemrograman Go (Golang)! Pada bagian ini, kita akan belajar membuat program sederhana dan mengenal sintaks dasarnya.

## 1. Program Hello World

Setiap belajar bahasa pemrograman, biasanya kita memulainya dengan menampilkan teks di layar komputer. Di Golang, kita menggunakan *package* bawaan bernama `fmt`.

```go
package main // Deklarasi package utama

import "fmt" // Mengimpor package fmt untuk melakukan input/output

func main() {
    // Fungsi utama yang akan dijalankan pertama kali
    fmt.Println("Hello, World!")
}
```

### Cara Menjalankan Program:
Jika kode di atas disimpan di dalam file `main.go`, jalankan di terminal menggunakan perintah:
`go run main.go`

## 2. Variabel dan Konstanta

### Variabel
Variabel adalah tempat untuk menyimpan data. Di Golang, ada beberapa cara mendeklarasikan variabel:

```go
package main

import "fmt"

func main() {
    // 1. Deklarasi dengan keyword 'var' dan menyebutkan tipe datanya
    var nama string = "Budi"
    
    // 2. Deklarasi dengan 'var' tanpa menyebutkan tipe datanya (Type Inference)
    var umur = 20
    
    // 3. Deklarasi singkat menggunakan ':=' (Hanya bisa di dalam function)
    pekerjaan := "Programmer"

    fmt.Println("Nama saya:", nama)
    fmt.Println("Umur:", umur)
    fmt.Println("Pekerjaan:", pekerjaan)
}
```

### Konstanta
Konstanta adalah nilai yang **tidak bisa diubah** setelah dideklarasikan. Cocok untuk data pasti seperti nilai Pi, dll.

```go
package main

import "fmt"

func main() {
    const phi = 3.14
    // phi = 3.15 // ERROR: nilai konstanta tidak dapat diubah

    fmt.Println("Nilai Phi:", phi)
}
```

## 3. Tipe Data Dasar

Beberapa tipe data yang wajib diketahui di Golang:
- **String**: Teks (contoh: `"Halo"`)
- **Integer**: Angka bulat (contoh: `10`, `-5`) -> Tipe data `int`.
- **Float**: Angka desimal (contoh: `3.14`) -> Tipe data `float32` / `float64`.
- **Boolean**: Bernilai benar (`true`) atau salah (`false`) -> Tipe data `bool`.

---
[⬅️ Kembali ke Daftar Isi Utama](../README.md) | [Lanjut ke Materi Array dan Slice ➡️](../02-Array-dan-Slice/README.md)
