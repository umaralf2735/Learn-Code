# 02 - Ilusi Array & Kekuatan Gaib "Slice" 

Kalau kamu belajar Golang tapi ngga tau bedanya Array dan Slice... Berhenti! Kamu akan bunuh diri di lapangan produksi. Inilah letak pondasi utama pengolahan Data Gede si Golang.

## 1. Array Beneran (Si Kolot Kaku)

Array Golang murni itu **SANGAT KAKU**. Slot yang kamu pesen diawal segitu, YAUDAH SELAMANYA GABISA DIGEDEIN ATO DIKECILIN. Ini makan memori tapi sangat aman buat hal statis (Kaya hari senin sampe minggu, kn cumn ada 7 kotak).

```go
// 1. Pesan Loker besi kaku isi 3 aja! Gabisa ditambah lg ya!
var papanSkor [3]int

papanSkor[0] = 50
papanSkor[1] = 95
papanSkor[2] = 20
// papanSkor[3] = 10 !! ❌ ERROR! LOKER FULL MENTOK! ARRAY OUT OF BOUNDS!

fmt.Println("Isi lokernya:", papanSkor)
```

## 2. SLICE: The Transformer (Sang Loker Dinamis)

Puyeng dong kita di Backend kalo narik database datanya bertambah terus, masa slot array gabisa direnggangin? Jangan khawatir, lahirlah `SLICE`. SLICE itu sejatinya "kacamata gaib" yang membungkus array biar dia elastis molor kesana kemari.

Syntax Slice cirinya gampang: **KURUNG SIKUNYA BLONG KOSONG `[]`**

```go
func main() {
    // PERHATIIN PAKE WALRUS `:=` DAN SIKUNYA GA PUNYA NOMER BLAS KOSONG []. Ini artinya SLICE AKTIF!
    belanjaanBuTejo := []string{"Bawang", "Celor", "Gincu"}

    // KARENA INI SLICE. LU BEBAS NAMBAH SLOT MENGGUNAKAN JURUS `APPEND`!!
    belanjaanBuTejo = append(belanjaanBuTejo, "Iphone 15")
    belanjaanBuTejo = append(belanjaanBuTejo, "Lamborghini")

    fmt.Println(belanjaanBuTejo)
    // TARA!! ISINYA BISA 5 BIJI TANPA DI COMPLAIN KEKURANGAN KOTAK!
}
```

### 🧠 Apa Yang Terjadi Dibelakang Layar (Rahasia Slice `append`)?
Waktu array aslinya kepenuhan... Si Slice `append` ini dengan sakti akan **Meng-Copy Paste seluruh isi array lama, menyewa lokasi Ram Baru 2x lipat lebih longgar, naruh datanya. Dan Membuang Array lamanya dari RAM!!** Terus berulang kek gitu ngedobel melar. 

Ibarat Kepompong ular yang ganti kulit! Hebat bukan? Oleh kerena itulah fungsi di Backend ngambil Database 100% menggunakan kotak `[]Slice` ketimbang Array kuno pelit.

---
[⬅️ Sebelumnya: Variabel Bawaan](../01-Dasar-Dasar/README.md) | [Lanjut ke Sorting Algoritma ➡️](../03-Algoritma-Dasar/README.md) | [🏠 Daftar Isi](../README.md)
