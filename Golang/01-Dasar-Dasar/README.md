# 01 - Dasar-Dasar Golang (Sang Kecepatan Cahaya)

Selamat datang di dunia Google Go (Atau sering dipanggil **Golang**). Bahasa ini diracik oleh ilmuwan raksasa Google dengan misi tunggal: *"Membunuh kelambatan bahasa OOP Tua dengan kecepatan roket rakitan ala Bahasa C, tapi tetap seenak Python diketiknya"*.

## 1. Tulang Punggung Utama (Pabrik Package & Import)

Sama kek bahasa kompilasi lainnya (C/Java). Golang itu ngga jalan sekedar script selembar. Dia di jalankan utuh sebagai *Paket App*.

```go
// 1. DIATAS SENDIRI WAJIB PAKETNYA (Karena ini file jalannya, dipanggil 'main')
package main

// 2. Kita manggil Gudang Alat Bawaan dari dalem komputernya ("fmt" = Format / Print)
import "fmt"

// 3. PINTU GERBANG UTAMA DI EKSEKUSI !! HARUS function main(){}
func main() {
    
    // Perhatikan, P dan L Nya Huruf gede!! (PrintLine). 
    fmt.Println("Halo Dunia Golang! Mesin V8 Melesat..")
    
}
```
**Analogi**: Ibarat kamu merakit robot. Baris `package` itu badan robotnya, `import` itu kamu masangin baut sama tangan mekaniknya, dan `func main` adalah **Batrai Utama tempat aliran listrik nylala pertama kali**!

## 2. Inisiasi Variabel (Perang `= vs :=`)

Golang itu tipenya mutlak gak suka dikibulin! Kalau string ya string selamanya! JS mah masi suka ngeletoy.

### A. Cara Kolot (Penuh Syariat Tipe Bawaan)
```go
// Namanya sapa, terus Tipenya Apa jelas. Trz di isi sama dengan = .
var namaJagoan string = "Satria Garuda"
var levelDewa int = 99
var udahMati bool = false
```

### B. CARA SAKTI MODERN GOLANG `:=` (Si Penebak Sakti Walrus Operator)
Orang google paling males ngetik banyak. Mereka bikin operator *Assignment Babi Ngepet* `:=` (Walrus/Titik-Tanya-Sama-Dengan).

```go
func main() {
    // Ga perlu pake tulisan VAR.. Ga perlu pakai tulisan INT !!!
    // Golang lgsg deteksi secara ghaib dan ngeborgol mutlak kalau duitPundi ini otomatis INT!!
    duitPundi := 5000 
    
    // duitPundi = "Ribuan" // ❌ KALO LU TIMPA STRING. TETAP ERROR MERAH DIKICK COMPILER! 

    // Output Interpolasi (Cetak)
    fmt.Printf("Bentar, si jagoan masi punya receh rp %d\n", duitPundi)
    // Tanda %d / %v itu adalah "Sediakan Slot Kosong Disini" yg diisi variabel ujung koma..
}
```

> ⚠️ **HUKUMAN MUTLAK DEWA GOLANG**: Kalau kamu bikin Variabel misal `baju := "Merah"` TAPI KAGA ELU PAKE SAMA SEKALI DIBAWAHNYA (Nganggur gadi-Print dlsb)... Program **ERROR GA MAU JALAN!!** Menghindari sampah RAM! Mantap ketat!!

---
[Lanjut ke Slice Memory ➡️](../02-Array-dan-Slice/README.md) | [🏠 Daftar Isi](../README.md)
