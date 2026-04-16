# 07 - Modul dan Senjata Rahasia (`pip`)

Bila Go pake go.mod, Ruby pake Gem, JS pake Npm. Maka Python kebanggaannya adalah `pip`!

## Menyedot Kecerdasan Buatan dari Luar (Pip)

Python itu terkenal karena AI-nya, Data Sciencenya, dsb. Itu semua merupakan Library Luar! Buat download kamu jalanin ini di terminal (Asal python path dah masuk):

```bash
pip install requests
```

Seketika komputermu punya skill `requests` yang kuat buat narik Data Rest API dari Website/Layanan manapun cuman modal `import`.

## Menggabung Berkas Lokal (Import antar Python)

File 1: `kalkulator.py`
```python
def kali_dua(angka):
    return angka * 2
```

File 2 Main: `aplikasi_saya.py`
```python
# Cukup gini aja tanpa ketik titik slice ./ apa apa 
import kalkulator 
# Atau biar pendek:
# from kalkulator import kali_dua

print("Saya manggil dari file sebelah:", kalkulator.kali_dua(5))
```
Betapa tenangnya hidup ini menyusun Project besar berlembar lembar menjadi folder folder modul terpisah!

---
[⬅️ Sebelumnya: Pemrograman Class](../06-Pemrograman-Class/README.md) | [Lanjut ke Error Handling ➡️](../08-Error-Handling/README.md) | [🏠 Daftar Isi](../README.md)
