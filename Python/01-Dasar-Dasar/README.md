# 01 - Dasar-Dasar Python (Pesona Ular Berbisa)

Pernah bertanya-tanya kenapa Python adalah rajanya Kecerdasan Buatan (AI) Chatbot, Hackers, dan Analisis Data? Karena Python diciptakan dengan filosofi mutlak: **"Harus bisa dibaca oleh anak SD sejelas membaca novel bahasa Inggris"**.

Tidak usah mengingat-ingat kurung kurawal `{ }` atau nulis Titik Koma `;` di akhir baris yang menyiksa bathin itu!

## 1. Menampilkan Nyawa Pertama (`Print`)

Mirip seperti bahas lain, kita minta program ngoceh:

```python
# Komen di python pakek pagar ya bang.
# Liat, KAGA PUNYA titikkoma sama skali kan dibelkang?
print("Halo Dunia, aku sedang belajar si Ular Berbisa ini!")

# Matematika kilat gak usah deklarasi aneh-aneh:
print("Kalo bapak ngutang sejuta dikurang 300rewe berarti sisa: ")
print(1000000 - 300000)
```

## 2. Variabel Misterius (Tipe Angka Bebas Ganti Baju)

Ini letak kesaktian Python. Kalo di **C atau Java**, kamu pusing harus milihin tipe baju Variabel misal `String KTP` atau `int Nomer`. 

Python itu **Dynamic Typing**, sebetulnya dia punya Tipe Data, TAPI disembunyiin dibelakang layar dan Ular ini yang pinter secara Gaib meramal Tipe datamu saat isiannya kamu tuang. Kayak wadah es krim yang bisa dipake naruh sate!

```python
x = "Siswa Magang"       # Komputer diem diem tau aslinya ini String
y = 10                   # Komputer otomatis merubah y jd Integer

# Wah bisa lgsung dicetak ditumpuk lhooo!
print("Bocah ini", x, "tp umurnya baru", y)

# 🚨 SIFAT RENTAN ULAR BERBISA
y = "Mendadak aku ganti tulisan!" 
# Python CUEK AJA, angkanya hilang dr memori dan y berubah mnjdi TEXT! (Javascript juga mirip gni pelupa).

```

## 3. Rahasia `f-string` (Nempel Teks & Nyisipin Data Mudah)

Salah satu hal paling ribet jaman dulu nulis Python adalah gabungin dua kalimat terpisah sama spasi. Sekarang, biasakan nulis huruf `f` (Format) tepat di depan KUTIP kalian!!

```python
namaJagoan = "GatotKaca"
levelSekarang = 99
hp_darah = 450.5 

# TANPA HURUF 'f': Pusing koma dan plus nya !!
# print("Kabar duka dari " + namaJagoan + " dia mati di lepel " + str(levelSekarang))

# PAKE HURUF 'f': (Masukin variabelnya dlm Kurung Kumis {  } !! SUPER RAPIH! )
ucapanMaut := f"Gila! Pertarungan epic {namaJagoan} berdarah {hp_darah} tamat d lv {levelSekarang} !!"

print(ucapanMaut)
```

Inilah awal kenapa pemula sejagat raya jatuh cinta seketika sewaktu beranjak kesini dari bahasa `C` atau `Java`. Karena sintaks nya gak ribet dan ga perlu manggil-manggil `#include` pusing di atasnya pas mau print teks sederhana!

---
[Lanjut ke Struktur Kontrol ➡️](../02-Struktur-Kontrol/README.md) | [🏠 Daftar Isi](../README.md)
