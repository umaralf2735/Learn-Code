# 06 - Pointer (Gerbang Ilmu Hitam Penembus Memori)

Jangan lari dulu! Kata "Pointer" emang bikin merinding anak Informatika semester 2 gara-gara bahasa C/C++. Tapi percaya deh, Pointernya Golang itu **10x lebih jinak** karena GA ADA yang namanya *Pointer Arithmetic* (ngitung selisih lokasi memori +1 +2). Cuma dipakai sebagai jalan tikus biar Data raksasa ngga Kecopy 2x.

## 1. Trik Irit Bensin: Pass-By-Reference 
Bayangkan kamu punya variabel tipe Data Karyawan lengkap 100 biji. Terus kamu masukin data itu ke dalem `FungsiA()`. 

Secara default, fungsi itu bakal **MEMPHOTO COPY** 100 biji karyawan itu kedalem FungsiA. Jadi RAM mu terbuang sia sia jadi 200 space!! Nah ini kebodohan yang harus dihindari!
Makanya kita gunakan **Pointer (Jalan Tikus Memori)**. Jadi yg di kasi ke Fungsi itu "ALAMAT KATA SANDI LOKASINYA AJA", Bukan dicopy datanya!! RAM mu cuma terpakai 101 space!

## 2. Meminjamkan Alamat dengan Simbol `&` (Ampersand) dan `*` (Bintang)

* `&` (Ampersand) = Bang, tolong buatin aku PIN Alamat lokasi letak kordinat barang ini yak!
* `*` (Asterisk) = Bang, PIN Alamat ini gw serahin ya, Coba lu teleport masuk bongkar brangkas isinya!

```go
package main
import "fmt"

// FUNGSI INI NGGA NERIMA ANGKA BANG! 
// Dilihat dr tandanya ( *int ), dia cuman NERIMA KERTAS TULISAN PIN ALAMAT dari variabel Int!
func GantiBanBocor( pinAlamatKordinat *int ) {
    
    // Karena ini pegang pin Alamat beneran si Mobilnya, kita bisa ngHACK!
    // KITA TEMBAK PAKAI (*) LAGI UNTUK NGE BONGKAR RUMAH ASLINYA!
    *pinAlamatKordinat = 100
    
}

func main() {
    banTekananNyata := 50 // Variabel Original (Lokasi ASli!)
    
    // ❌ SALAH BGT CLONE / PASS BY VALUE:
    // GantiBanBocor( banTekananNyata )  
    
    // ✔️ BENAR PASS BY REFERENCE: Lemparin (Kertas Pin Kordinat nya!) Pakai Dan '&'
    GantiBanBocor( &banTekananNyata )
    
    // GILA! TEKANAN NYATA DI LUAR FUNGSI SEKARANG BERUBAH JADI 100 !!!! 
    // FUNGSI TADI BERHASIL NGEHACK MASUK LEWAT JALAN TIKUS!!!!
    fmt.Println(banTekananNyata) 
}

```

Ilmu inilah yang digunakan untuk menjaga Aplikasi Cloud (GCP/AWS) kalian tetap irit RAM 1GB meskipun memproses Jutaan Data dalam 1 waktu!! Karena gampang, semua Backend Dev cinta Go.

---
[⬅️ Sebelumnya: Fungsi](../05-Fungsi/README.md) | [Lanjut ke Class OOP KW (Struct) ➡️](../07-Struct-dan-Method/README.md) | [🏠 Daftar Isi](../README.md)
