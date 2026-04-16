# 02 - Struktur Kontrol dengan Indentasi

DIBAHAS DI SINI BAHWA PYTHON BENCI KURUNG KURAWAL `{}` !
Kalau C pake itu, Python mewajibkan kamu menggeser spasi dengan rapi (Indent / Titik Dua ` : `).

## 1. Percabangan Bikin Merinding

Lihatlah betapa anggun kodenya :

```python
nyawa_game = 40

if nyawa_game > 50:
    print("Wah aman dong broo, santai")
elif nyawa_game > 20: 
    print("Oke lumayan")
else:
    print("Sekarat gais! Minum Potion!")
```
Penting! Kalau tulisan `print` nya ga dikasih **1 buah Tab spasi alias nggak dimajukan ke kanan**, program mu akan ERROR sintax!!!

## 2. Looping For dengan Range
Untuk ngulang angka ga pake i++.

```python
# Berhenti di angka 5 (tapi ga masuk limanya) => [0,1,2,3,4]
for angka in range(5):
    print("Tarik napas ke", angka)
```

Sip, asalkan ingat "Indentasi Geseran Spasi Tab", Python mu akan tenang berjalan mulus.

---
[⬅️ Sebelumnya: Dasar-Dasar](../01-Dasar-Dasar/README.md) | [Lanjut ke Koleksi Data ➡️](../03-Koleksi-Data/README.md) | [🏠 Daftar Isi](../README.md)
