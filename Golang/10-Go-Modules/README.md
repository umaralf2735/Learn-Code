# 10 - Go Modules (Manajemen Package)

Ketika kode yang kalian buat hanya sebatas `main.go`, maka itu baru dianggap script iseng. Jika proyeknya sudah mulai bercabang menggunakan library orang lain dari internet (contoh: driver database, router Gin), maka kamu butuh yang namanya **Go Modules**.

Ini seperti NPM di NodeJS atau Composer di PHP.

## 1. Membuat Project Baru

Buka terminal di dalam foldermu, lalu jalankan:

```bash
go mod init belajar-golang
```

Perintah di atas akan menciptakan *1 buah file sakti* bernama `go.mod`. File ini fungsinya seperti KTP untuk aplikasimu. Dia sadar kalau ini project buatanmu bernama "belajar-golang" dan mencatat library apa saja yang bakal kamu sewa dari luar.

## 2. Menarik Library Orang Lain

Coba kamu buka website *pkg.go.dev* dan temukan jutaan modul siap pakai. Anggaplah kita ingin memakai router web super kilat bernama `Gin`.

Kita bisa mengetikkan:

```bash
go get -u github.com/gin-gonic/gin
```

Tiba-tiba otomatis library `gin` tersebut akan ter-download ke komputermu, dan nama library-nya akan tercatat pada file `go.mod` dan `go.sum`. 

## 3. Import Package Milik Sendiri

Dengan Go Modules, kamu bisa mengimport kode-kode fungsi yang telah kamu pisah di folder lain ke dalam `main.go`.

**Folder `math/kalkulator.go`**:
```go
package math

// FUNGSI HARUS DIAWALI HURUF BESAR agar bisa dipanggil dari luar (Public)
func Tambah(a, b int) int {
    return a + b
}
```

**File Utama `main.go`**:
```go
package main

import (
    "fmt"
    // Panggil nama module tadi ditambah foldernya
    "belajar-golang/math" 
)

func main() {
    hasil := math.Tambah(100, 50)
    fmt.Println(hasil)
}
```

Selamat! Kamu sudah memiliki dasar kuat untuk menjadi *Backend Engineer* Golang.

---
[⬅️ Sebelumnya: Error Handling](../09-Error-Handling/README.md) | [🏠 Daftar Isi Utama](../README.md)
