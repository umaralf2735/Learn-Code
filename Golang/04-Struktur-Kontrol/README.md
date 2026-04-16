# 04 - Struktur Kontrol (Tanpa Kurung Bertele-Tele)

Kata orang Google pencipta Golang: *"Kami muak ngetrik Kurung Biasa `()` pada IF dan FOR ! Buang semuanya jadi Polosan!"*

## 1. Percabangan Bersih Mengkilat `if - else`

Nggak usah repot ngetik kurung leher biasa di samping tulisan `if` ny!

```go
func main() {
    uangTabungan := 50000

    // Gak Pake Kurung Biasa kan? Bener bener Telanjang murni lgsg Kondisinya
    if uangTabungan > 100000 {
        fmt.Println("Sikatt beli ayam bakar kmpung!!")
    } else if uangTabungan > 20000 {
        fmt.Println("Mending masak mie di kosan gan hemat.")
    } else {
        fmt.Println("Sabar, puasa senin kamis dapet pahala.")
    }
}
```
*Note mutlak:* Kurung kurawalnya `{` **HARUS nempel bersejajar sama if nya di baris itu juga.** Kalau kamu enter turunin kebawah.. Golang bakal ngamuk merah Error Compiler! Makanya program Go seluruh dunia itu gaya ngetiknya setipe identik karena udah diatur tuhan Go.

## 2. FOR Adalah Tuan Tanah Terakhir! (GAK ADA WHILE DI GO!)

Di C / C# / Pyhton / Java kalian kenal `While(bla)`. Go menghapusnya selamanya. "Buat apa ada banyak jenis perulangan? Pakai For aja buat Segala Situasi!!"

### A. FOR Gaya Standar Ngitung Anak Tangga
```go
// Tetap ga dipakein Kurung Leher biasa lhoo!
for i := 1; i <= 5; i++ {
    fmt.Println("Loncat ke - ", i)
}
```

### B. FOR Menyaru Jadi While
```go
bensinKendaraan := 5

// Tinggal buang inisiasi dan incrementnya... Tara!! Terlihat kyak While kan jadinya haha.
for bensinKendaraan > 0 {
    fmt.Println("Brem brem nrocos jalaannn sisa bsnin...", bensinKendaraan)
    bensinKendaraan--
}
```

## 3. Switch Case Menembus Zaman (No Break!)
Kelamahan terbesar Switch di C / JS / Jav adalah... KALAU LU LUPA NGETIK TULISAN `break;` , MISTERI FATAL BAKAL JALAN SEMUA BARIS BAWAHNYA SAMBUNG MENYAMBUNG KESELEK.

Golang memperbaikinya: **Otomatis Berhenti (Break) pada 1 Pilihan Mutlak!**

```go
jurusanAnak := "TKJ"

switch jurusanAnak {
case "RPL":
    fmt.Println("Coding mulu gapernah mnyntuh duni nyta!!")
    // GAK PERLU DIKASIH BREAK; !!!
case "TKJ":
    fmt.Println("Napas lu bau debu ngerakit kabel tiang mulu!!")
default:
    fmt.Println("Wah gatau gue anak mana ni bocah.")
}
```

Inovasi Inovasi inilah yang bikin developer tua manapun yang nyentuh golang bakal *Nangis Terharu* mensyukuri betapa ringannya beban otak nyusun alibi code haha!

---
[⬅️ Sebelumnya: Sort Logika](../03-Algoritma-Dasar/README.md) | [Lanjut ke Mesin Fungsi ➡️](../05-Fungsi/README.md) | [🏠 Daftar Isi](../README.md)
