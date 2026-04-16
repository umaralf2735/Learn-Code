# 06 - Pemrograman Objek Python (Class)

Kalau sebelumnya Ruby memakai `@`, Javascript memakai `this.`. Ada yang tahu pengganti ajaibnya di Python? Yak, kata `self`!

## Merajut Cetakan Ular

Kalau kamu mau bikin fungsi dan simpen data didalam tubuh Class-nya, parameter awalnya **selalu dan harus diberi tulisan `self`**. Baru diikuti nama inputan lain.

```python
class Kucing:
    # Metoda gaib '__init__' akan terpanggil ketika kamu bikin Kucing() baru! 
    # (Persis sama kyk constructor lah)
    def __init__(self, nama_panggilan, rasnya):
        # Tempelkan data ke self (diri Class ini sendiri!)
        self.nama = nama_panggilan  
        self.ras = rasnya          

    # Method / Fungsi biasa
    def nge_meong(self):
        print(f"Meowww... aku ini {self.nama} spesiesnya {self.ras} bangettt!!")


# Mari cetak kuenya!!
kucing_oren = Kucing("Si Oren", "Kucing Pasar")
kucing_bule = Kucing("Bella", "Anggora")

kucing_oren.nge_meong()
```

Kunci memahami OOP di python hanya 1: Semua fungsi didalam yang menyangkut parameter wajib mendata `self` didepan parameter pemanggillannya, titik.

---
[⬅️ Sebelumnya: Algoritma Dasar](../05-Algoritma-Dasar/README.md) | [Lanjut ke Modul dan PIP ➡️](../07-Modul-dan-Pip/README.md) | [🏠 Daftar Isi](../README.md)
