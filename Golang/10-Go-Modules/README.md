# 10 - Belanja Senjata Perusahaan Luar (Go Modules)

Menempel pada Ekosistem luar. Jika JS punya NPM (Node Package Manager). Jika Python nggembok pakai PIP. Go meracik sistem super rapi bernama `Go Modules` yang bener-bener jadi standar industri saat ini (Semenjak Go versi lawas di drop supportnya gara2 GOPATH ribet).

Kalau Go versi Jadul, kamu harus naruh Projek mu di *C:/Users/Go/src/...* aduh menyedihkan lah haha. Sekarang BEBAS!

## 1. Nyalain Nadi Projectmu (`go mod init`)

Pertama kali bikin folder Project (Misal Backend Tiktok). Buka Terminal CMD mu. Ketik ini 1x seumur idup folder.

```bash
go mod init nama-website-lu.com/backend
```

*BOOM!* Tercetaklah Akte Kelahiran Sakti yang wujudnya bernama `go.mod`. Intip isinya, pasti cuma ngasih tau "Oh dia ngerun di versi Go v1.18..."

## 2. Nyedot Pustaka Raksasa API Dari Internet (`go get`)

Misal boss mu nyuruh kamu bikin sistem Chat Web Socket / Framework REST API super ngebut namanya Fiber. Kita tarik paksa ilmu nya dr luar pakai `get`.

```bash
go get -u github.com/gofiber/fiber/v2
```

Seketika file `go.mod` mu isinya bertambah nama pendaftar package baru + Muncul file hantu checksum (`go.sum`) menjaga agar versimu tidak dirusak sama orang usil yang ngehack lewat package yang sama.
*(Asiknya di Go itu GA ADA FOLDER NODE_MODULES yang gedenya sampe 1 GB nyampah dikomputermu!! Go mengelolanya dan numpuk di alam ghaib AppData sistem rapi dan sangat efisien!)*

## 3. Pake Sihirnya Di Kode Utama Main File

```go
package main

// Liat! Sekarang tulisan Import nya ngambil dari GITHUB DOT COM Asik bgt !!
import (
    "log"
    "github.com/gofiber/fiber/v2" 
)

func main() {
    app := fiber.New() // Manggil Objek framework besarnay

    app.Get("/", func(c *fiber.Ctx) error {
        return c.SendString("Buset, Baru Bab 10 belajarnya udah jadi Website Backend Kencengan Golang Cuk!")
    })

    log.Fatal(app.Listen(":3000"))
}
```

SELAMAT!!!! TAMAT!!! Kamu kini setara dengan *Backend Engineer Mid-Level* Google / Start-up Internasional. Cukup pahami dan perdalam Konsep Conccurency mu. Maka bayaran belasan jt perbulan ngurus API Golang siap menghampiri dompet pemula sperti kalian ini!

---
[⬅️ Sebelumnya: Dosa dan Defer Panic](../09-Error-Handling/README.md) | [🏠 Daftar Isi Utama Golang](../README.md)
