# 07 - Golang Gak Punya Class! (Struct & Method)

"Terus kalau gw mau bikin game musuh bos nya beda beda darah level giman dong kalo gada Class?!"
Hahaha, Golang memang membunuh kata *Class Inheritance*. Mereka menggantinya dengan gaya perakitan (Composition) make `Struct`.

## 1. Struct (Cetakan Data Bisu)

Tugas struct cuman nampung bentuk formatnya doang. Dia ga bisa diisi *logic* atau *function*.

```go
type Hero struct {
    NamaLengkap string
    Nyawa       int    // Ingat pakai huruf besar didepan kalau mau dipanggil dr file luar!!
    SenjataDewa string
}

func main() {
    // Nguasain cara nyeplaknya
    jagoanGue := Hero{
        NamaLengkap: "GatotKaca",
        Nyawa:       9000,
        SenjataDewa: "Otot Kawat", // koma dibelakang tetap wajib wlw di akhir
    }
    
    fmt.Println("Lariiiii ada si", jagoanGue.NamaLengkap)
}
```

## 2. Ngetem Punggung (Method / Receivers)

Bagaimana cara masukkin `fungsi` kedalem Cetakan Hero itu? Golang memakai jurus *Receiver*. 
Fungsinya ditempel di PUNGGUNG si Class. Mirip seperti Benalu.

Perhatikan bedanya Function Biasa dengan Function yg Nempel di punggung struct (Disebut: **Method**).

```go
// ... dari struct Hero di atas

// LOGIKAN NYA DISERLIPKAN DI ANTARA FUNC DAN NAMA FUNGSI!!!!
// (h *Hero)  -> BACANYA: Fungsi ini numpang di punggungnya siapapun yg tipenya HERO!
// Catatan Dewa: Selalu gunakan (Pointer *Hero) kalau fungsi ini ngerubah data asli didalemnya (Kek motong nyawa).

func (h *Hero) KenaJebakanBatman() {
    h.Nyawa -= 50
    // Liat, aku bisa lgsung nembak (h.Nyawa) miliknya dia sndiri! Ga lwt parameter.
    fmt.Printf("Waduh %s kepleset kulit pisang. Nyawa trsisa %d\n", h.NamaLengkap, h.Nyawa)
}

func main() {
    pahlawanSatu := Hero{ NamaLengkap: "GatotKaca", Nyawa: 100 }
    
    // PEMANGGILAHN NYA PUN SEKARANG MULUS PAKE TITIK (DOT . ) PERSIS KAYA CLASS OOP MODERN
    pahlawanSatu.KenaJebakanBatman()
    pahlawanSatu.KenaJebakanBatman()
    
    // Karena Pakai (*) Pointer Receiver ditas tadi, Nyawa beneran berkurang mnjd 0 wkwk!
}

```

Tanpa kata kunci konyol layaknya `this` atau `self` (Python/JS). Golang merapikan kodingan puluhan ribu baris di Microservice nya lewat Trik punggung ini! Mantap jiwa.

---
[⬅️ Sebelumnya: Memory Pointer](../06-Pointer/README.md) | [Lanjut ke Kekuatan Terbesar GO (Goroutine) ➡️](../08-Goroutine-dan-Channel/README.md) | [🏠 Daftar Isi](../README.md)
