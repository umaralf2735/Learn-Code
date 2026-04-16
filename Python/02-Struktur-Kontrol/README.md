# 02 - Struktur Kontrol & Kengerian Makna Spasi (Indent)

PYTHON SANGAT MEMBENCI KURUNG KURAWAL `{ }`. 

Di bahasa Javascript/C++, lu bebas nulis kode ngacak spasi berantakan kedalem karena pembatas wilayah kodenya dilindungi kurung kurawal. 

**DI PYTHON TAB SPASI ADALAH HUKUM MURNI!!** Kalau geser lu ga lurus masuk se-tab.. MATI ERROR PROGRAM LU!!

## 1. Percabangan dengan `if`, `elif`, dan `else`

Kata ganti `else if` di-singkat manja jadi murni 4 huruf: `elif`. Dan gerbangnya dibuka pake TITIK DUA `:`.

```python
saldoku = 0

# Pintu pembuka pake ( : ), dan isinya WAJIB MASUK MENDORONG KE KANAN 1 TAB!
if saldoku > 50000:
    print("Sikat, makan mekdi mas brok!!")
elif saldoku > 15000:
    # Lihat menjorok masuknya? Jika kmu iseng ngetik Print di ujung kiri... Error!
    print("Warkop indomie aja gan, aman.")
else:
    print("Haduh... mending nelen ludah lu bro...")

print("Woy aku di ujung kiri nih! Aku selalu kepanggil meskipun IF nya ga ada yg cocok karena aku bebas dr penjara TAB d atas!")
```

## 2. Looping For dengan sihir `range()`

Buang jauh-jauh angan nulis perulangan C murni kayak ngetik batas `for (int i= 0; i<5; i++)` njlimet! Di python kalian pakai pendaftar ajaib bernama `range(BatasAngka)`.

```python
# BACANYA: Ulangin i, sediain daftar list ngantri dari 0 berenti di LIMA (Tapii ga masuk limanya).
for angka in range(5):
    print(f"Mengocok telur putaran ke: {angka}") 

# OUTPUT DI TERMINAL: Mngocok tlur ke 0, 1, 2, 3, 4! (ingat kan index komputer mulai hitngan Dr 0?)
```

## 3. Looping While (Tunggu sampai miskin)

Kalo kondsinya gk ketauan angka batesnnya, while jawra nya!
```python
bensinMobil = 5

while bensinMobil > 0:
    print(f"Jalan-jalan sore asik bawa pajero. Bensin tinggal {bensinMobil}")
    bensinMobil -= 2 # Boros coy skali ngegas abis 2 liter
    
print("Udah, mati mongok ditengah jalan.") 
```

**Satu Pesan Sponsor:** Berhati hatilah pakai Text Editor, pastikan mode *Tab=4 Space* mu nyala. Jutaan Programmer luar frustasi ngurus kode Python orang lain gara gara beda cara ngetik Tab spasi nya (ada yg pke tab Keyboard nyata, ada yg di teken Spasi 4x). Python Benci ketidaksamaan ini!

---
[⬅️ Sebelumnya: Dasar-Dasar](../01-Dasar-Dasar/README.md) | [Lanjut ke Koleksi Data List ➡️](../03-Koleksi-Data/README.md) | [🏠 Daftar Isi](../README.md)
