# 03 - List & Dictionary (Pisau Bedah Data Science)

Bagaimana cara menaruh seluruh identitas 20,000 pasien rumah sakit tanpa ngetik manual let x1, let x2, x3? Python dipuja-puja para *AI Researcher* gara gara sistem pengerukan Datanya (Array) luar biasa mudah dikendalikan!

## 1. List (Mantan Preman Array Siku `[]`)

List di python itu gak ribet. Bisa ngadain berbagai macam jenis ukuran dan nyampur (String, Int, Boolean disatuin di wadah yg sama).

```python
# Loker gaib yg bs nyimpan apa aja
keranjangPasar = ["Telur Ayam", "Sawi Hijau", "Bawang", 99]

// --- SIHIR MANIPULASI (SLICING PIZZA!) -- 
print("Barang no 1:", keranjangPasar[1]) # Sawi (Ingt kn msuknya dr no 0)

# 🌟 NGAMBIL DARI BAKANG TANPA TAU ISI TOTALNYA!! 
print("Barang paling ujung:", keranjangPasar[-1]) 
# KEREN KAN?! Pake angka minus (-) artinya lu nyedot array lgsg dri pantat keblakang! (-1 brarti ujung mentok= Pny laci si angka 99) 

# NAMBAH DIBLAKANG 
keranjangPasar.append("Panci Gosong")
print(keranjangPasar)
```

## 2. Dictionary (Tas Ajaib Berkantong Label `{}`)

Mirip banget Object Javascript ato Struct Golang. Dia dibungkus pake kumis `{ }` dan ada *Key: Value* kunci namanya, biar gampang nyarinya gak usah hapal nomer kotak angka list nya.

```python
profilTersangka = {
    "namaKtp": "Joko Sumbing",
    "umurReak": 35,
    "buronan": True,
    "kasusMalu": ["Maling Ayam", "Ngelarikan Kucing Warga"]
}

# Ngambil datanya cmn panggil string kuncinnya (Case Sensitive lu)
print("Yang dicari bernama:", profilTersangka["namaKtp"])

# Ngorek array dalem dictionary!
print("Berapa kasus si joko?", len(profilTersangka["kasusMalu"])) 

# Merubah atau Nambah Data Mendadak klupaan!
profilTersangka["kotaAsal"] = "Bekasi"
print(profilTersangka) 
```

Semua data yg dilempar mesin AI, ChatGPT, atau Sensor Cuaca di Bumi manapun... Wujud mentahnya saat masuk Python akan dirubah bentuk persisis menjadi *Dictionary `{}`* ini! Jadi bersahabatlah dengannya.

---
[⬅️ Sebelumnya: Struktur Kontrol](../02-Struktur-Kontrol/README.md) | [Lanjut ke Fungsi ➡️](../04-Fungsi/README.md) | [🏠 Daftar Isi](../README.md)
