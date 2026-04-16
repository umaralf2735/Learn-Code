# 07 - Modul dan Senjata Rahasia Dunia Luar (`pip`)

Bila Golang pake `go mod`, Ruby pake `Gem`, JS pake `Npm`. Maka Python menamakan sekte perpusatakaannya dengan ejaan tiga huruf dewa: **`pip`** (Pip Installs Packages).

Tanpa Pip. Ular mu cuman ular sawah cacing tak berbisa. Tapi kalo lu install library dari komunitas MIT Harvard AI.. Ularmu bkl brubah jdi Naga Machine Learning!

## 1. Menyedot Kecerdasan Buatan dari Luar (Pip)

Untuk memanggil dewa komunitas open source. Buka terminal (CMD) mu (Asal python path dah masuk, ntar auto punya pip jg koq).

```bash
# Bayangkan pingin narik data Rest API kenceng, gak perlu narik ribet logic socket murni .
pip install requests
```

Seketika komputermu mengundah script `requests` dan punya skill mencengkram internet tanpa ampun.

```python
import requests

# BOOOM! Tiga baris kodingan narik berita koran d dunia maya!! 
res = requests.get("https://jsonplaceholder.typicode.com/todos/1")
print(res.json())  
```

## 2. Menggabung Berkas Lokal (Modul File Sesama Python)

Kira kira kalo file app mu isinya 50,000 baris, gila aja mau scroll nya. Pisahin jd file berbeda dong!!

File 1: `kalkulator.py` (Disimpen se-folder dgn file utama bawahnya).
```python
# Ini cumn isinya ilmu logic tanpa ngerun jalan utana
def kali_dua(angka):
    return angka * 2
    
def pajakMaut(duid):
    return duid * 0.11
```

File 2 Main Utama: `aplikasi_saya.py`
```python
# CARA 1: NYEDOT SEGELONDONGAN FILENYA UTUH!!
import kalkulator 
print("Saya manggil dr file mangkuknya:", kalkulator.kali_dua(5))

# --- ATAUUUU --- 

# CARA 2: NYEDOT SELEKTIF YANG DIBUTUHIN AJA (Lebih IRIT RAM!!!)
from kalkulator import pajakMaut
print("Langsung panggil gapake nma file nya ! ", pajakMaut(150000) )
```

Sangat bersih nyusun project pake Python kan. Tinggal `import` beres no ribet. 

---
[⬅️ Sebelumnya: Pemrograman Class OOP](../06-Pemrograman-Class/README.md) | [Lanjut ke Jebakan Error ➡️](../08-Error-Handling/README.md) | [🏠 Daftar Isi](../README.md)
