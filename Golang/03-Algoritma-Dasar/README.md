# 03 - Algoritma Dasar (Sorting & Searching)

Agar dapat memecahkan masalah nyata, kita perlu belajar Algoritma. Algoritma adalah urutan langkah logis untuk memecahkan suatu masalah. Dua contoh algoritma klasik adalah algoritma untuk **mengurutkan (Sorting)** dan **mencari (Searching)**.

## 1. Algoritma Pencarian (Linear Search)

Linear search (Pencarian Linier) adalah metode mencari nilai di dalam kumpulan data dengan mengecek satu per satu elemen dari awal sampai akhir.

```go
package main

import "fmt"

// Fungsi untuk mencari sebuah nilai 'target' di dalam slice 'data'
func linearSearch(data []int, target int) int {
    for i, nilai := range data {
        if nilai == target {
            return i // Kembalikan index tempat target ditemukan
        }
    }
    return -1 // Target tidak ditemukan
}

func main() {
    angkaKita := []int{50, 30, 20, 90, 70}
    angkaYangDicari := 90

    indexDitemukan := linearSearch(angkaKita, angkaYangDicari)

    if indexDitemukan != -1 {
        fmt.Printf("Angka %d ditemukan pada index %d\n", angkaYangDicari, indexDitemukan)
    } else {
        fmt.Println("Angka tidak ditemukan.")
    }
}
```

## 2. Algoritma Sorting (Pengurutan)

Pernahkah kalian memiliki data acak dan ingin diurutkan dari yang terkecil ke terbesar? Ada banyak teknik Sorting, dan mari kita mulai dengan **Bubble Sort** (salah satu algoritma paling sederhana, namun sangat logis untuk pemula).

### Bubble Sort

Algoritma ini dinamakan *bubble* karena elemen yang nilainya paling besar akan diletakkan di akhir perlahan-lahan (seperti gelembung yang mengapung ke atas).

Prinsip kerja:
Bandingkan elemen saat ini dengan elemen di sebelahnya. Jika elemen saat ini lebih besar dari sebelahnya, tukar (*swap*) posisinya. Ulangi terus menerus sampai tidak ada elemen yang ditukar lagi.

```go
package main

import "fmt"

// Fungsi untuk melakukan bubble sort
func bubbleSort(arr []int) {
    n := len(arr)
    
    // Looping sebanyak jumlah elemen didalam array/slice
    for i := 0; i < n-1; i++ {
        
        // Looping untuk mencari jika ada yang berjejer tidak tersusun
        for j := 0; j < n-i-1; j++ {
            
            // Apakah elemen saat ini lebih besar dari elemen setelahnya?
            if arr[j] > arr[j+1] {
                // Tukar (Swap) jika ya
                temp := arr[j]
                arr[j] = arr[j+1]
                arr[j+1] = temp
                
                /*
                Cara swap yang lebih ringkas di Golang:
                arr[j], arr[j+1] = arr[j+1], arr[j]
                */
            }
        }
    }
}

func main() {
    daftarAngka := []int{64, 34, 25, 12, 22, 11, 90}
    fmt.Println("Sebelum diurutkan:", daftarAngka)
    
    bubbleSort(daftarAngka)
    
    fmt.Println("Setelah diurutkan: ", daftarAngka)
}
```

Bagaimana? Perlahan-lahan algoritma akan menukar angka paling besar ke kanan sampai semuanya terurut dengan rapi!

---
[⬅️ Sebelumnya: Array dan Slice](../02-Array-dan-Slice/README.md) | [🏠 Daftar Isi](../README.md)
