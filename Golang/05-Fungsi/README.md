# 05 - Fungsi (Function)

Fungsi sangat berguna untuk memisahkan kode yang panjang menjadi blok-blok kecil yang bisa dipakai berulang kali. Jadi kalau ada proses yang sama, tidak perlu dibikin ulang, panggil saja fungsinya!

## 1. Fungsi Sederhana

```go
package main

import "fmt"

// Fungsi bernama sapaan
func sapaan() {
    fmt.Println("Halo, selamat datang di program ini!")
}

func main() {
    // Memanggil fungsi sapaan
    sapaan()
    sapaan() // Bisa dipanggil berkali-kali!
}
```

## 2. Fungsi dengan Parameter

Kita bisa memberikan data ke dalam fungsi agar bisa dimanipulasi di dalam fungsi tersebut. Data ini disebut argumen atau parameter.

```go
package main

import "fmt"

// Fungsi yang meminta 2 parameter tipe int: a dan b
func hitungJumlah(a int, b int) {
    hasil := a + b
    fmt.Println("Hasil penjumlahan:", hasil)
}

func main() {
    hitungJumlah(10, 20) // a bernilai 10, b bernilai 20
    hitungJumlah(5, 5)   // a bernilai 5, b bernilai 5
}
```

## 3. Fungsi yang Mengembalikan Nilai (Return)

Bukannya langsung *print* ke layar, terkadang kita ingin fungsi itu bekerja memproses data, lalu "mengoper" hasil hitungnya ke kita untuk disimpan. Kita dapat menggunakan fungsi *return value*. Jangan lupa harus mencantumkan tipe data kembaliannya.

```go
package main

import "fmt"

// Fungsi ini akan minta a dan b, lalu MENGEMBALIKAN tipe data 'int'
func perkalian(a int, b int) int {
    hasil := a * b
    return hasil // Wajib mengembalikan kembalian bernilai int
}

func main() {
    // Hasilnya kita simpan kedalam variabel
    hasilSimpan := perkalian(4, 5)
    fmt.Println("Tolong ambilkan ini:", hasilSimpan)
}
```

### Multiple Return Values

Paling mantap, Golang bisa mengembalikan lebih dari 1 hasil dalam 1 fungsi!

```go
package main

import "fmt"

func luasDanKeliling(sisi int) (int, int) {
    luas := sisi * sisi
    keliling := 4 * sisi
    return luas, keliling
}

func main() {
    L, K := luasDanKeliling(5)
    fmt.Println("Luas:", L, "Keliling:", K)
}
```

---
[⬅️ Sebelumnya: Struktur Kontrol](../04-Struktur-Kontrol/README.md) | [Lanjut ke Materi Pointer ➡️](../06-Pointer/README.md) | [🏠 Daftar Isi](../README.md)
