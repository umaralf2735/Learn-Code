# 04 - Fungsi di Python (Def)

Untuk mencegah spaghetti kodingan panjang panjang.

## Rumus Asli Keyword Limit

Python cukup pakai keyword 3 huruf nama `def` (Definition).

```python
def panggil_tukang_pijit(nama_bos):
    print(f"Halo tukang urut, dapet pesanan buat kerumah Bos {nama_bos} sekarang!")

panggil_tukang_pijit("Yanto")
```

## Return yang Tak Tahu Diri (Positif)

Python bisa mereturn 2 atau 3 angka berbeda di fungsi tanpa di deklarasi macem-macem didepan fungsinya kaya Golang, bebas sebebas bebasnya!! Pucuknya dipisah Koma.

```python
def pertukaran_matematika(a, b):
    tambah_semua = a + b
    kurang_semua = a - b
    
    return tambah_semua, kurang_semua

# nyimpennya otomatis dipisah ke dua keranjang yang tergeletakan
hasil1, hasil2 = pertukaran_matematika(10, 3)

print("Kalau ditambah nilainya", hasil1) # 13
print("Kalau dikurang nilainya", hasil2) # 7 
```

Singkat padat merayap dan tak ribet!

---
[⬅️ Sebelumnya: Koleksi Data](../03-Koleksi-Data/README.md) | [Lanjut ke Algoritma ➡️](../05-Algoritma-Dasar/README.md) | [🏠 Daftar Isi](../README.md)
