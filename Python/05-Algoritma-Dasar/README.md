# 05 - Algoritma Dasar Python (Kemewahan Modern)

Siapapun yang menyusun data science menggunakan python tentu dilarang keras mengetik kode algoritma primitif untuk menyaring Data! Kita akan pakai metode bawaan C-Compiled Python yang super kilat.

## 1. Sorting (Cukup `.sort()`)

```python
angka_acak = [500, 10, 5, 9999]

# Menyusun Array/List secara menaik
angka_acak.sort() 
print(angka_acak) # Keluarnya [5, 10, 500, 9999]

# Menyusun terbalik turun
angka_acak.sort(reverse=True)
```

## 2. Searching di List Object Python

Sama seperti metode pencarian dengan Lambda. Python menggunakan *List Comprehension* yang bacanya super nyaman kek baca novel.

```python
murid = [
    {"nama": "Andi", "nilai": 50},
    {"nama": "Budi", "nilai": 95},
    {"nama": "Wati", "nilai": 88}
]

# Ambil SISWA YANG LULUS diatas KKM!
# Bahasanya: Bikin list kumpulan 'm' DIMANA 'm' diputar dalam murid kalau 'm' poin nilainya > 75
lulusan_hebat = [m for m in murid if m["nilai"] > 75]

print("Yang lulus nih bos:")
for anak in lulusan_hebat:
    print("-", anak["nama"])
```

Penyaringan data (`Filter/Search`) itu paling sakti dipakai List Comprehension yang kayak rumus metamatika di atas tadi!

---
[⬅️ Sebelumnya: Fungsi](../04-Fungsi/README.md) | [Lanjut ke Class Python ➡️](../06-Pemrograman-Class/README.md) | [🏠 Daftar Isi](../README.md)
