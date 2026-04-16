# 03 - Algoritma Sort Bawaan (Mengalahkan C)

Memang di bahasa C kita harus mengasah logika bikin Bubble Sort *of O(N^2)* manual muterin i dan j... itu keren buat di kuliahan sih...

**TAPI DI DUNIA KERJA**, ngetik begituan itu buang waktu (menghabiskan gaji developer). Golang sudah berterima kasih karena memberikan satu paket Pustaka (Package) sakti khusus meratakan Array: yaitu Package `sort`.

## Nyusun Data Primitif Dalam 1 Baris!

```go
package main

import (
    "fmt"
    "sort" // WAJIB DI IMPORT PISAU SAKTINYA!!
)

func main() {
    kardusAngka := []int{100, 5, 2, 9999, 10}

    // 1. Sort menaik secara elegan kilat kilauan :
    sort.Ints(kardusAngka) 

    fmt.Println("Nah Rapi kan tuh Bos naik: ", kardusAngka) 
    // Jawab: [2, 5, 10, 100, 9999]


    // 2. KALO MAU GA SENGUE NGURUT TERBALIK KAYA HARGA TERMAHAL BAGAIMANA??
    // Bungkus dlu array pake jubah (Reverse) lalu suapi ke mangkuk Sort td!
    sort.Sort(sort.Reverse(sort.IntSlice(kardusAngka)))
    
    // TARA! JAWABAN JADI: [9999, 100, 10, 5, 2]
    fmt.Println("Dari yg paling gila angkanya:", kardusAngka)
}
```

## Memecah Kode Data Object Berat Majemuk

Pasti lo bertanya-tanya, kalau datanya berupa Struktur (`struct`/Dictionary JSON) yang bentuknya kotak-kotak misal Sort Murid berdasarkan Gaji... Gimana cara ngasih tau Golang bahwa "Woi, sort ini pake atribut umur ya! bukan namanya!" ??

Golang pny kekuatan sakti Sorting buatan Kustom (*Slice Stable Sort!*).
```go
import (
    "fmt"
    "sort"
)

// Bayangin ini Struct Cetakan Mahasiswa (Ntr di pelajri belakangan tenang aja)
type Pekerja struct {
    Nama string
    Gaji int
}

func main() {
    listUmat := []Pekerja{
        {"Jaelani", 500},
        {"Wawan", 9000},
        {"Anas", 20},
    }

    // NYUSUN BERDASARKAN OBJEK (Pake Jurus Sort.Slice)
    // Ngasi Logika Lemparan Ke Mesinnya: Wahai mesin sort.. Aku anggap data ke (i) menang klo gjinya lbh kcil dr(j)..
    sort.Slice(listUmat, func(i, j int) bool {
        return listUmat[i].Gaji < listUmat[j].Gaji
    })

    fmt.Println("Di urut dr yg termiskin:", listUmat)
    // Bkl terurut jd -> Anas, Jaelani, Wawan lho!
}
```

Bagi yg paham ini, seluk beluk Database Sorting API akan lumer dimakan logic backend mu dengan gampang.

---
[⬅️ Sebelumnya: Slice vs Array](../02-Array-dan-Slice/README.md) | [Lanjut ke Loop Kontrol Ekstrem ➡️](../04-Struktur-Kontrol/README.md) | [🏠 Daftar Isi](../README.md)
