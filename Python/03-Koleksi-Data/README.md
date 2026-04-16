# 03 - Koleksi Data Maut Python

Kekuatan AI dan Data Science Python tidak ada artinya sebelum mereka punya `List` (Array) dan `Dictionary`.

## 1. List (Mantan Array biasa)
Pakai kurung siku standar `[]`.

```python
kendaraan = ["Motor", "Mobil", "Bajaj"]

kendaraan.append("Pesawat") # Menambah ke belakang

# memutar pakai In!
for x in kendaraan:
    print("Ayo naik:", x)
```

## 2. Dictionary (Kamus Mapnya Python)
Bila ingin data berkolom identitas, ini mirip struct / JSON-nya JS. Memakai kurung siku melengkung `{}`.

```python
biodata = {
    "nama": "Agus Sugih",
    "sekolah": "SMK Hebat",
    "kelas": 12
}

print(biodata["nama"])    
# OUTPUT HANYA MUNCUL = Agus Sugih

biodata["umur"] = 18 # Menambahkan property baru lho, gampang banget!
```

Dan inilah kedua hal yang nanti kalau kalian gabung (List of Dictionaries), sangat mantap untuk ngambil api json balikan!

---
[⬅️ Sebelumnya: Struktur Kontrol](../02-Struktur-Kontrol/README.md) | [Lanjut ke Fungsi ➡️](../04-Fungsi/README.md) | [🏠 Daftar Isi](../README.md)
