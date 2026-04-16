# 08 - Goroutine & Channel (Mahkota Emas Golang)

Inilah alasan utama kenapa Tokopedia, Gojek, Bukalapak 100% bergantung pada Golang Backend.
**CONCURRENCY**. Bagaimana menjalankan 1.000 Pekerjaan secara bersamaan tanpa nge-hang laptop?

Dulu di JS buat ngakalin gini pake `Async Await`. Di Java Pake `Threads` yg berat minta ampun RAM nya.
Golang ngeluarin **Goroutine**, *Thread Mini super cacing ringan*. Bahkan Laptop Intel Celeron butut bisa menspawn 500,000 Goroutine bersamaan!

## 1. `go` (Kata kunci sakti pecah tubuh Naruto)

Kamu punya fungsi kirim email, loadingnya lama 3 detik. Bikin komputer diem nunggu.
Sihir aja, kasih tulisan depannya `go ` ....

```go
package main

import (
    "fmt"
    "time"
)

func KirimEmailSelesai() {
    time.Sleep(3 * time.Second) // Pura-pura loding beratttt 3 detik
    fmt.Println("📧 Email Ke Mantan Terkirim!")
}

func main() {
    fmt.Println("AKSI DIKLIK!!")
    
    // 🌟 MANTRA DEWA! 
    // Go akan memecah bayangan baru, nyuruh bayangannya ngerjain fungsi ini di Alam Paralel Murni!
    go KirimEmailSelesai() 
    
    fmt.Println("Main ke warung ah mumpung nunggu dia kelar nge-load...")
    
    // KARENA PROGRAM UTAMA GOLANG NYA (func Main) keburu beres dititik terbwah sblm 3 detik!
    // KITA HARUS TAHAN PINTU PERSEGI PANJANG INI BIAR GAK KETUTUP CEPET2 !
    time.Sleep(5 * time.Second)
    fmt.Println("-- Pintu Utama Golang Berakhir Tutup --")
}

/* HASIL PRINT NYA:
AKSI DIKLIK!!
Main ke warung ah mumpung nunggu...
(SETELAH 3 DTK)
📧 Email Ke Mantan Terkirim!
(SISA 2 DTK)
-- Pintu Utama Golang Berakhir Tutup --
*/
```

## 2. Channel (Pipa Paralon Komunikasi Antar Bayangan)

Kalau Naruto mecahin diri ngirim Kloningan (`go KirimEmail()`), gimana si Bayangan itu laporan ke Naruto Asli kalo Kerjannya Udah Kelar trus mo ngirim Uang hasil buruan bayangnnnya balik? 
Ayo kita Pesen Pipa Paralon `channel` pake kata `make`.

Liat Tanda Panah `<-` yang jadi ikon Sakral Golang disini:

```go
func AnakBuahCariUang(pipaMasukinUangnya chan int) {
    fmt.Println("Bos, sy mulung botol bentar..")
    time.Sleep(2 * time.Second)
    
    // Pake panah ngarah ke pipanya (Masukin ke paralaon!!)
    pipaMasukinUangnya <- 150000 
}

func main() {
    // 1. Toko Pipa Material (Bikin Pipa yang cuma muat dilewatin integer)
    pipaUang := make(chan int)
    
    // 2. Spawn Anak Buah ke Alam Go Paralel nya! Sambil nyodorin pipanya!
    go AnakBuahCariUang(pipaUang)
    
    // 3. DI FUNGSI MAIN NARUTO NAMPUG DI UJUNG PARALON BAWAH NYA NUNGGUIN SAMPE JATUH (Panah kearah variabel dr pipa!!)
    uangCairBos := <- pipaUang  // ✨ PROGRAM DI MAIN GABAKAL TEMBUS KESINI KALO SI ANAK BUAH BLOM NGIRIMIN KESINI!!
    
    fmt.Println("Hore cair cair dapet jatah ", uangCairBos)
}
```

Bab ini adalah **"Holy Grail" / Cawan Suci** Programmer Go. Memahaminya membuat Gaji kamu layak setara Sr. Backend Systems. Pengerjaan Video Render/Scrape ribuan Toko di Tokopedia terjadi dalam milidetik gara-gara trik 10.000 Coroutine ini jalan Paralel nyerang bareng lalu dilaporkan via Pipa. Sangat Mengagumkan.

---
[⬅️ Sebelumnya: Struct Class Asli](../07-Struct-dan-Method/README.md) | [Lanjut ke Penangkapan Error ➡️](../09-Error-Handling/README.md) | [🏠 Daftar Isi](../README.md)
