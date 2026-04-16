# 04 - Fungsi di Python (Pekerja Mesin Pabrik)

Kita bikin gerbang supaya gausah ngoding berulang ulang. Cukup pakai kata pengantar *Definition* (`def`).

## 1. Rumus Merakit Mesin Kecilnya

```python
# Fungsi nerima 2 isian bahan mentah: nama dan nominal sumbangan
def alatPengerasSumbangan(namaPenyumbang, nominal):
    # Mesin Memproses...
    pajak = nominal * 0.1
    bersihUang = nominal - pajak
    
    # Kalo lu lupa ngetik TAB buat baris dibawah ini.. mesin gagal kebongkar!
    print(f"Bpk {namaPenyumbang} dermawan memberikan kotor {nominal}. Trmksh.")
    
    # Return ngembaliin data yg di olah dr dlm mesin (Uang Bersi) ktangan penangkap!
    return bersihUang


# Manggil / Neken Tombol Msinnya Trus nadangin hasil Return nya!
hasilGereja1 = alatPengerasSumbangan("Coki", 50000)
hasilMesjid = alatPengerasSumbangan("Rizky", 1000000)

print(f"Uang brsi bersih trkumpul {hasilGereja1 + hasilMesjid}")
```

## 2. The Power of `*Args` & `**Kwargs` (Karung Ghaib Bebas Isi)

Sering kesal bikin fungsi tp gak tau brapa banyak input angkanya?
Gunakan sihir Bintang 1 (*Tuple*) atau Bintang 2 (**Dictionary**) buat melempar sampah parameter berapapun yg lu mau gajelas panjangnya lgsung terisep dan jadi array Karung!!

```python
# Tulis bintang di depan! Brti fungsi ngisep bberpapun org ngisi diblkng k koma!
func totalinBelanjaGw(*semuaBarangGw):
    rajaHasil = 0
    
    # Muterin isi Karungnya pakai in !
    for harga in semuaBarangGw:
        rajaHasil += harga
        
    return rajaHasil

# Tembak ngasal aja jumlahnya BEBEBASS, ga ditolak!! 
print("Total struk ke-1: ", totalinBelanjaGw(100, 50, 10))        # isi 3 buah 
print("Total struk ke-2: ", totalinBelanjaGw(2000, 500, 7000, 1)) # isi 4 buah jg MSUK!!
```

Ini adalah senjata rahasia Framework Python (seperti Django atau Flask), karena mereka nerima lemparan opsi form Web yang jumlah *Input formnya* bisa sangat bervariatif dari pengguna tanpa nge-crash fungsi backend nya.

---
[⬅️ Sebelumnya: Koleksi Data List](../03-Koleksi-Data/README.md) | [Lanjut ke Algoritma Ghaib ➡️](../05-Algoritma-Dasar/README.md) | [🏠 Daftar Isi](../README.md)
