# 06 - Pointer di Golang

Pointer terkadang menjadi materi yang menakutkan bagi pemula, namun ia sangat penting di Golang. Pada dasarnya, **Pointer adalah cara untuk mengetahui "Alamat Rumah" dari sebuah data di memori komputer.**

## Konsep Dasar (Pass by Value)

Secara bawaan (*default*), Golang itu menganut **Pass by Value**. Artinya, ketika kita memasukkan variabel ke variabel lain, atau ke sebuah fungsi, Golang akan **Menduplikasi/Mengkopi** datanya.

```go
package main

import "fmt"

func ubahSuhu(suhu int) {
    suhu = 40 // Niatnya mau ngubah suhu panas
}

func main() {
    suhuSaya := 25
    ubahSuhu(suhuSaya)
    fmt.Println(suhuSaya) 
    // OUTPUT: 25. Kenapa ngga berubah jadi 40? 
    // Karena fungsi 'ubahSuhu' hanya dikasih DUPLIKAT aslinya aja!
}
```

## Memasuki Pointer (Pass by Reference)

Agar fungsi bisa ngedit data **aslinya** secara langsung (bukan duplikatnya), kita harus kasih fungsi tersebut "Alamat" memorinya. 
- Simbol `&` (Ampersand): Digunakan untuk mengambil alamat memori (Pointer).
- Simbol `*` (Asterisk): Digunakan di depan alamat, artinya kita "Bongkar/Akses isi rumahnya" langsung.

```go
package main

import "fmt"

// Menggunakan tipe *int (Pointer ke int)
func ubahSuhuAsli(suhu *int) {
    *suhu = 40 // Mengubah isi dari memori secara langsung
}

func main() {
    suhuSaya := 25
    fmt.Println("Sebelum:", suhuSaya) // 25
    
    // Berikan 'Alamat' suhuSaya ke fungsinya dengan &
    ubahSuhuAsli(&suhuSaya)
    
    fmt.Println("Sesudah:", suhuSaya) // 40
}
```

Sekarang kamu sudah memanipulasi data tanpa menduplikatnya. Cukup efisien, apalagi kalau ukuran datanya besaaaarr!!

---
[⬅️ Sebelumnya: Fungsi](../05-Fungsi/README.md) | [Lanjut ke Materi Struct ➡️](../07-Struct-dan-Method/README.md) | [🏠 Daftar Isi](../README.md)
