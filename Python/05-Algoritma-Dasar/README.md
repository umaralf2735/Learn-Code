# 05 - Algoritma Dasar Python (Kemewahan List Comprehension)

Karena python adalah bahasa dewa untuk nyari Pola Big Data. Ga mungkin ilmuwannya nyuruh lu nge-Loop pake For biasa baut nyarik nilai angka terkecil, kan?

Inilah bab perpaduan kekuatan mutlak fungsi Bawaan (*Built-in*) di Python.

## 1. `.sort()` VS `sorted()`  (Mengurutkan Kekacauan)

Awas! dua benda kembar ini bedaa kerjanya!
* `.sort()`    == Ngebunglon! *Ngelancurin List Asilnya* yg ada dimemori diacak ganti permanen dengan rapi! Dosa bagi File Original!
* `sorted()` == Nge-Photocopy! List Aslinya utuh aman. Dia mulangin Data Cerminanya yg udh rapi ke tmpat bru.

```python
poinGamer = [500, 10, 5, 9999, 100]

# --- 1. PHOTCOPY (Hasil Copy-an Baru)
cerminanRapi = sorted(poinGamer)
print("Yg rapi clone :", cerminanRapi)       # [5, 10, 100, 500, 9999]
print("Buktinya aslinya ga brubah :", poinGamer) # Masih Berantakan 500 td didepan !


# --- 2. DESTRUKTIF RE-ARRANGE (Ngacak memori)
poinGamer.sort(reverse=True) # Merusak memori jd dr gede -> kecik

print("Aslinya Skramg brubah rusak :", poinGamer)  # Udah bnrn keganti! [9999, 500, 100, 10, 5]
```

## 2. Sihir 1 Baris:  *List Comprehension*

Pernah kalian disuruh: *"Ubah array list gaji orang2 jadi POTONGAN PAJAK 10% kedalam list baru, tpi bwt orang yg Gajina Diatas 5 JT aja!"* 

Kalo pk bahasa Go / C kalian butuh belasan baris for dan if. Di pyton cukup 1 baris yang dibacanya kek pmbahasan soal sosiologi novel !!

```python
semuaGaji = [3000000, 15000000, 5500000, 2000000]

# 🌟 RUMUS PUSING NYA =  [BENTUK YANG MAU DISIMPEN]  for (iterasi tunggal) in (SUMBERNYA)   if (SYARATNYA)

pilihanYgDiPajakin = [ (g * 0.1) for g in semuaGaji if (g > 5000000) ]

print(pilihanYgDiPajakin)
# OUTPUT TERJADI SUPER KILAT : [1500000.0, 550000.0]
# Krn yg ksrting cma gaji ke-2 (15 jt) sm ke-3 (5,5jt). 
```

Semakin kalian bisa nebak teka-teka The List Comprehension diatas dalam hitungan 2 detik mikir di kepala, semakin gila value diri lu bisa ditarik masuk kedalam Divisi Data Engineer Machine Learning perusahaan raksasa Gojek / Tokped dan Bank! List Comprehension adalah kunci surga array di Python!

---
[⬅️ Sebelumnya: Fungsi Mesin](../04-Fungsi/README.md) | [Lanjut ke Class Python ➡️](../06-Pemrograman-Class/README.md) | [🏠 Daftar Isi](../README.md)
