# 06 - Pemrograman Objek (Class dan Sang Mahluk `self`)

Kalau di Javascript memakai `this.`, di PHP memakai `$this->`. Ada yang tahu pengganti ajaibnya di Python? Yak, kata mutlak `self`! Pemula biasanya muntah disini kok ada parameter ga berguna yang nongol di setiap fungsi Class nya? Padahal gak diminta loh! 

Tenang, itu karena Python beda aliran OOP dengan Java.

## 1. Merajut Cetakan Kue (Blueprint Class)

Kalau kamu mau bikin fungsi method yang nempel ke class, parameter awalnya **selalu dan harus diberi tulisan `self`**. Baru diikuti nama inputan aslinya.

```python
class Kucing:
    # 1. METHOD SAKRAL (Constructor) = Yg dpanggil otomatis persis saat cetak dr pabrik! 
    # Persis sama kyk constructor di class Javascript JS ES6.
    def __init__(self, nama_sihir, rasnya):
        # Nempelkan data isian ke tubuh 'self' (diri Class ini sendiri!)
        self.nama = nama_sihir  
        self.ras = rasnya          

    # 2. Method / Tindakan Biasa (Tetep ada self lho awas jgn dihapus!)
    def nge_meong(self):
        print(f"Meowww... aku ini {self.nama} spesies bangasawan {self.ras} bangettt!!")
        
    def dielusMajikan(self, namaMajikan):
        print(f"Purr purrr.... mksih nak bos {namaMajikan}.. {self.nama} ngantuk nih..")

```

> **Kenapa `self` ditaruh situ padahal ga dipanggil diluar bos?**
Karena secara rahasia kalau di ranah python, waktu lu manggil objeck misal `Kucing.nge_meong()`, Mesin ular itu diem-diem sebenernya nerjemahin mnjadi `Kucing.nge_meong( kucingKuSebagian )` . Oleh karena itulah parameter ke-0 harus ditampung wadah yg nyimpen referensi dirinya sendiri. Logis kan si Ularnya.


## 2. Mencetak Objeknya (Instatiation)

Ingat, Python gapunya kata sihir `new` kaya Java JS ato C++ ya. Lngsung panggil Namanya!

```python
# Mari cetak kuenya!! Tanpa NEW langsung nama CLASS () !!! Mantaap!
kucing_oren = Kucing("Si Oren", "Kucing Pasar")
kucing_bule = Kucing("Bella", "Anggora")

# Memanggil Sifat Uniknya (Ekslusif milik diri sndiri tida mnyngkut yg blh!)
kucing_oren.nge_meong()

kucing_bule.dielusMajikan("Joko Subiyanto")
```

Semua hal yang lu liat dipython, List, Dictionary, Inteher Tuples. Sebenernya dibalik layarnya mereka cumn sebuah CLASS Python Murni wkwk! (Everything is Object in Python).

---
[⬅️ Sebelumnya: Algoritma Comprehension](../05-Algoritma-Dasar/README.md) | [Lanjut ke Menyedot Modul PIP ➡️](../07-Modul-dan-Pip/README.md) | [🏠 Daftar Isi](../README.md)
