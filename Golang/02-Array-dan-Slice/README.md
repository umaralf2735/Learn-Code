# 02 - Array dan Slice di Golang

Dalam pemrograman, kita sering memerlukan tempat untuk menampung banyak data. Di Golang, kita punya dua struktur data dasar untuk melakukannya: **Array** dan **Slice**.

## 1. Array

Array adalah kumpulan data yang bertipe sama dan memiliki **ukuran tetap**. Jika kita membuat array dengan 5 elemen, ukurannya tidak bisa dikurangi atau ditambah lagi.

### Deklarasi dan Penggunaan Array

```go
package main

import "fmt"

func main() {
    // Deklarasi array panjang 3 dengan tipe string
    var namaHari [3]string

    // Memasukkan data ke index array (index dimulai dari 0)
    namaHari[0] = "Senin"
    namaHari[1] = "Selasa"
    namaHari[2] = "Rabu"

    fmt.Println(namaHari[0]) // Output: Senin
    fmt.Println(namaHari)    // Output: [Senin Selasa Rabu]
    
    // Deklarasi array sekaligus inisialisasi datanya
    nilai := [4]int{80, 90, 75, 100}
    fmt.Println(nilai)
}
```

## 2. Slice

Slice sangat mirip dengan Array, bedanya **ukuran Slice bersifat dinamis**. Anda bisa menambah ukuran elemen kapan saja sesuai kebutuhan. Slice sejatinya merupakan referensi ('potongan') dari suatu array di belakangan layar.

### Deklarasi dan Penggunaan Slice

Untuk mendeklarasikannya, gunakan format yang sama dengan Array tetapi **jangan tuliskan** ukurannya di dalam kurung siku `[]`.

```go
package main

import "fmt"

func main() {
    // Array: var arraySaya = [3]int{1, 2, 3}
    // Slice:
    sliceSaya := []int{10, 20, 30}
    
    fmt.Println("Isi Slice:", sliceSaya)

    // Menambah data baru ke dalam slice dengan fungsi append()
    sliceSaya = append(sliceSaya, 40)
    sliceSaya = append(sliceSaya, 50, 60) // Menambah beberapa nilai sekaligus

    fmt.Println("Setelah ditambah:", sliceSaya)
    // Output: [10 20 30 40 50 60]
}
```

### Membuat Slice dari Array

Kita juga bisa memotong sebuah Array menjadi Slice.

```go
package main

import "fmt"

func main() {
    bulan := [6]string{"Januari", "Februari", "Maret", "April", "Mei", "Juni"}

    // Membuat slice dari index ke-1 hingga sebelum index ke-4
    sliceBulan := bulan[1:4]
    
    fmt.Println(sliceBulan) // Output: [Februari Maret April]
}
```

---
[⬅️ Sebelumnya: Dasar-Dasar](../01-Dasar-Dasar/README.md) | [Lanjut ke Materi Algoritma ➡️](../03-Algoritma-Dasar/README.md) | [🏠 Daftar Isi](../README.md)
