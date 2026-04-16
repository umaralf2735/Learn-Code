# 08 - Goroutine dan Channel di Golang

Fitur paling mematikan (*killer feature*) dari bahasa Go dibandingkan bahasa PHP atau Node.js pada umumnya adalah ini: Manajemen antrian banyak hal sekaligus (Konkurensi).

## 1. Goroutine

Di dunia aslinya kalau kita punya 3 tugas (A, B, C) biasanya komputer jalanin A sampai kelar, baru B, baru C. 
Di Golang kita bisa jalankan ketiganya barengan tanpa takut ngelag karena Goroutine itu "Benang Eksekusi" yang ukurannya sangat ringan (Kecil sekali memori-nya)!

### Cara Menggunakan
Untuk menyuruh program jalan barengan di background, cukup tempel keyword `go` didepan pemanggilan fungsinya!

```go
package main

import (
    "fmt"
    "time"
)

func cetakPesan(jumlah int, pesan string) {
    for i := 0; i < jumlah; i++ {
        fmt.Println((i + 1), pesan)
        time.Sleep(100 * time.Millisecond) // Istirahat bentar
    }
}

func main() {
    // Kita jalankan fungsi secara Async dengan 'go'
    go cetakPesan(5, "Tugas Berat A jalan di Background!")
    go cetakPesan(5, "Tugas Berat B ikutan jalan!")

    // Ini jalan di fungsi utamanya
    cetakPesan(3, "Tugas Fungsi Main!")
    
    // Main akan selesai setelah baris ini! Dan goroutine akan ikut Matii!
}
```

## 2. Channel

Saat goroutine berjalan, mereka itu kayak ada di dimensinya masing-masing. Kalau kita mau goroutine A ngobrol/kirim data ke Main / Goroutine B, kita pakai **Channel** (Pipa Komunikasi).

```go
package main

import "fmt"

func masakMie(pipa chan string) {
    // Anggap waktu jalan 2 detik... terus mie matang!
    fmt.Println("Sedang mamasak dibelakang layar...")
    
    // Kirim pesan lewat pipa, pake tanda panah <-
    pipa <- "Mie Indomie sudah matang brooo!"
}

func main() {
    // Bikin pipa untuk jalur lewat string
    pesanChannel := make(chan string)

    // Mulai kerjakan tugas
    go masakMie(pesanChannel)

    // DI SINI PROGRAM MAIN AKAN BERHENTI (BLOCKED)
    // SAMPAI ADA ORANG NGELEMPAR DATA DARI PIPA...
    hasilLemparan := <-pesanChannel 

    fmt.Println("Pesan diterima:", hasilLemparan)
}
```
 
Dengan fitur ini di Go, server backend bisa menampung traffic ratusan ribu per detik dengan gampang banget!!

---
[⬅️ Sebelumnya: Struct](../07-Struct-dan-Method/README.md) | [🏠 Daftar Isi Utama](../README.md)
