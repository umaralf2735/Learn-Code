# 01 - Dasar-Dasar Python

Python itu ibarat menulis bahasa Inggris harian kepada PC kamu. Tipe data? Tidak usah pusing definisinya di awal!

## 1. Menulis Teks

Sama seperti Golang dan JS, cukup gunakan fungsi pamungkasnya `print`.

```python
# Tidak pakai titik koma ya bos (;) Haram hukumnya
print("Halo namaku Budi!!") 
print(50 * 5)
```

## 2. Peka akan Variabel

Tinggal simpan dan biarkan *ularnya* yang menebak dia itu String, Boolean (Huruf Awal Harus BEesar), atau Integer.

```python
x = "Mahasiswa Abadi" # otomatis jadi string text
y = 10                # otomatis Int
sudah_lulus = False   # Untuk boolean, hurufnya WAJIB besar (False / True)

# Nyetak gabungan:
print(f"Status dari si {x} ini padahal udah semester {y} loh. Dan kelulusannya: {sudah_lulus}")
# Note: Format 'f' (f-string) di awal petik itu berfungsi agar bisa menyisipkan kurung kurawal variabel ke text-nya!
```

---
[Lanjut ke Struktur Kontrol ➡️](../02-Struktur-Kontrol/README.md) | [🏠 Daftar Isi](../README.md)
