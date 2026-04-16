# 09 - Penanganan Error (Defer & Trik "Dosa Itu Data")

"Hah? Go ngga punya Try Catch kyk Java sama JS?! Gila bahaya dong kalo Database mati trs error?"

Tenang! Penemu Golang mengusung *Filosofi: Kesalahan (Error) adalah Barang Data Normal yang harus diperlakukan kayak variabel Biasa.*.

## 1. Dosa / Error Yang Di Retun Berbarengan Benda

Ini nyambung dengan Materi Multiple Return Value di Fungsi Bab 5 kemarin! Go memaksa kita ngecek di setiap baris.

```go
package main

import (
    "errors"
    "fmt"
)

// Kalau sukses brarti hasilnya Int, Kalau gagal dia memuntahkan wujud Error nya jg.
func TarikTunaiMesin(saldo, wd int) (int, error) {
    if wd > saldo {
        // Ciptakan Dosanya dan kirim! (Hasil int nya dikasih 0 (kosong))!
        return 0, errors.New("Woy duit gak cukup bro di saldo!!")
    }
    
    // Kalo aman Sentausa, DOSA NYA (error) LU BALIKIN KOSONG HAMPA ALIAS `nil`.!!
    return saldo - wd, nil
}


func main() {
    hasilTerbaru, dosaError := TarikTunaiMesin(100, 500)
    
    // BEGINILAH CARA GOLANG MAIN AMAN! (GA ADA TRY CATCH, DIA NGECEK MANUAL DOSA NYA KOSONG ATO ADA ISRINYA GA !! Bosenin emg ahhha)
    if dosaError != nil {
        fmt.Println("Bahaya Sistem Dihentikan Sementara, Alasan:", dosaError)
        return // Keluar!! Paksa tutup
    }
    
    fmt.Println("Sukses Duit kecacir sisa:", hasilTerbaru)
}
```

## 2. Sang Kata Kunci `defer` (Wasir Pembantu Yang Sabar)

Pernah kalian nulis script ngedobrak *Harddisk File IO* tapi kelupaan ngasih tulisan tutup (close)?! Memori laptop tumpah ruah alias bocor! (*Memory Leak*).

Go menciptakan `defer`. Kalo lu kasih ini, JAMINAN MUTLAK KODE INI BERJALAN TERKAHKIRAN MESKI PROGRAM MU KENA ERROR TENGAH JALAN ATAU RETURN MENDADAK!! 

```go
func BongkarFileRahasia() {

    fmt.Println("1. Berhasil Nyogol Ngebuka Gembok Brangkas PINTU DATABASE AWS!")
    
    // WAJIB SERTA MERTA SAAT ITU JUGA DETIK ITU JG NYURUH TUKANG BERSIH BERSIHNYA MASUK (DEFER)
    defer fmt.Println("3. DEFER JALAN: Tembok dipel, Brankas Database AKU TUTUP KEMBALI RAPAT-RAPAT!! AMAN!")
    
    // Nah bebas dah skrng u mau ngapain dibawah nnti defer bakal auto jln trpaling akhir
    fmt.Println("2. Proses ngambil ngambilin duit batangnya asik di DB...")
    
    errormati := true
    if errormati { 
        fmt.Println("ADA BOM MAU MELEDAKK!!! AKU KABURR DR GUDANG (RETURN)")
        return // Aku keluar dr Gudang ini!
    }
    
    fmt.Println("4. Baris baris abwah sini gabakal kesentuh lg!")
}

// Kalau Dijalankan Outputnya Bkal bgini : 
// 1. Berhasil Nyogol....
// 2. Proses ngambilngambilin..
// ADA BOM MAU MELEDAK AKU KABUR!!
// 3. DEFER JALAN: Tembok dipel... DATABASE AMAN DITUTUP.
```

Kalian Liat?? Meskipun program lari ditengah nengah make `return`. Pesan **DEFER** tetep jalan mutlak gabaikal di skip menjaga brankas / memori tetap tertutup bersih. Goks CANGGIH ABIS !

---
[⬅️ Sebelumnya: Gorotine Asynchornous](../08-Goroutine-dan-Channel/README.md) | [Lanjut ke Manajemen Framework / NPM Luar ➡️](../10-Go-Modules/README.md) | [🏠 Daftar Isi](../README.md)
