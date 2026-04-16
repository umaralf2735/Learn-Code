# 05 - Mesin Fungsi (Dewa "Pecah Telur" *Multiple Return*)

Memecah belah operasi besar di fungsi (*func*) adalah rahasia Microservice level AWS berjalan stabil. Kalau fungsi C / JavaScript biasa cuman memulangkan (return) SEBUAH 1 barang data tunggal... Di Go kamu bisa return berlusin-lusin balikan sekaligus dari 1 Fungsi!!

## 1. Syntax Fungsi Halus dan Default Parameter Belakang

Penempatan Label Type nya itu Unik, Bukan didepan, tapi DI BELAKANG nama parameternya wkwk. Ciri khas tulen Go.

```go
package main
import "fmt"

// Liat!  nama dulu -> baru Tipenya (string)
// Diluar Kurung param -> Tipe Kembalian nya sbg hasil (string)
func pesenGoFood(makanan string, harga int) string {
    notaGhoib := fmt.Sprintf("Pesanan %s sedang dimasak dengan uang tip %d yah", makanan, harga)
    return notaGhoib
}

func main() {
    bonTukang := pesenGoFood("Seblak Setan", 15000)
    fmt.Println(bonTukang)
}
```

## 2. Ilusi Pecah Belah Nilai Kembar (*Multiple Return Value*)

Trik inilah yang dipakai ribuan Driver Gojek pas koneksinya error balikan api. Kenapa? Karena di Go, setiap fungsi ngambil API Luar... dia ME-RETURN "HAHILNYA" BERSAMAAN DEGAN TIKET "STATUS ERRORNYA"!!

```go
// Tuh liat kembaliannya ada DUA DIKURUNG! = (int, int)
func aduPenaltiMatematika(a int, b int) (int, int) {
    hasilTambah := a + b
    hasilKali := a * b
    
    // Ngereturn Dua Barang disekat Koma 
    return hasilTambah, hasilKali
}

func main() {
    // NAHHHH... Waktu manggil, lu siapin DUA KERANJANG lgsg barengan nampung leparan dr sana!
    jwbPlus, jwbSilang := aduPenaltiMatematika(5, 10)
    
    fmt.Printf("Kalo ditambah jd %d. Oh.. tp kalau dkkali brarti %d", jwbPlus, jwbSilang)
    
    /* 
    CATATAN FATAL:
    Gimana kalau dari lemparan dua barang tsb, lu CUMAN BUTUH (hasilKali nya) dan ga peduli sm hasilTambah?
    Lu HARUS NGEBUANG BARANG SI hasilTambah KEDALAM TONG SAMPAH '_' (Blank Identifier). 
    
    Contoh:
    _, jwbSilangTok := aduPenaltiMatematika(9, 2)
    */
}
```

## 3. Fungsi Pukul Rata Variadic (Pake Titik-Titik Tiga `...`)

Suka kesel kalau pengen bikin fungsi "Hitung Total Pengeluaran", tapi parameternya gatau ada berapa jumlah tagihannya dlm 1 bulan?
Pakai Titik tiga diblakang (Variadic)! Pintu depan fungsimu melonggarkan batas terima argumen jadi BEBAS BRP PUN LU MAU KASIH!

```go
// "Hayo sini woi, setorin parameter berapapun, entar jd array integer (int) dalem perut gw!"
func hajarKalkulatorHitungTotal(tagihan ...int) int {
    
    totalDompet := 0
    // Mutar isi perutnya! (Tinggal pake for-range Array)
    for _, itemDuit := range tagihan {
        totalDompet += itemDuit
    }
    
    return totalDompet
}


func main() {
    // Wah gila, bisa manggil fungsi yg sama tapi diisi 3 Biji angka dan 5 biji Angka sekaligus njir!
    nota1 := hajarKalkulatorHitungTotal( 50, 10, 5) 
    nota2 := hajarKalkulatorHitungTotal( 100, 2, 80, 50, 999)
    
    fmt.Println(nota1) // 65
    fmt.Println(nota2) // 1231
}    
```
Sang dewa fleksibilitas! Dari sinilah framework backend besar dibangun kuat menopang request User yg jumlah key JSON nya random ga ketara!.

---
[⬅️ Sebelumnya: Struktur Kontrol](../04-Struktur-Kontrol/README.md) | [Lanjut ke Memory Pointer Sakti ➡️](../06-Pointer/README.md) | [🏠 Daftar Isi](../README.md)
