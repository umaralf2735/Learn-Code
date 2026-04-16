# 09 - Bermain Mengobrak-Abrik Berkas Teks (File I/O)

Membaca File TXT CSV atau Menyimpan hasil rekapan PDF itu kerjaan sehari-hari Python WebScraper/Hacker yang dapet data curian orang buat dispen ke dlm Harddisknya. Wkwk.

## 1. Pintu Bahaya (Membuka Berkas)
Cara bodoh yg sering dipake pemula:
```python
berkas = open("catatanku.txt", "w") # w artinya WRITE 
berkas.write("Tulis rahasia disini...")
# KALAN LUPA NULIS berkas.close() !!! (MEMORI BOCOR / FILE DIKUNCI MATI AMA SYSTEM!!)
berkas.close()
```

## 2. Pintu Ajaib Dewa Modern Mutlak: `with open`

Rahasia aman dari membongkar file `.txt` atau apapun biar komputermu memorinya gak bocor saat kalian "Lupa / Crash sblum nge-Close" filenya adalah pakai Metode Indentasi `with`.

```python
# Tulis dan Timpa isi Teks ("w" berarti WRITE / TULIS MENIMPA)
# Kalau ga mau nimpa Hapus yg lama melainkan pengen sambung teks ke BAWAH, pakailah ("a" atau APPEND)

with open("data_sakti.txt", mode="a") as file_ku:
    file_ku.write("Ini adalah teks baris pertama yg kusiaspkan!\n")
    file_ku.write("Semua rahasia nyimpen form disini juga..")
    
    # 🌟 MAGIC HAPPENS ! 🌟
    # PERHATIKAN: setelah batas TAB blok spasi ini habis menjorong ke KIRI luar lagi, 
    # file otomatis DITUTUP SENDIRi! GAK perlu lu panggil file_ku.close()!! GILA AMAN!!!


# CARA BACA NYEDOT BERKAS HARDDISK : Mode "r" (READ)
with open("data_sakti.txt", mode="r") as bukuku:
    semua_text = bukuku.read()
    
    print("====================")
    print("Isi buku berhasil disedot dr hdd:")
    print(semua_text)
    print("====================")
```

Dengan ilmu file IO ini, para Pembuat Virus Python biasanya menyisipkan script ini untuk ngopi *Password Local Browser* kalian, trus dia ngirim filenya pakai *Requests PIP Library* yang udah lu plajarin d bab sebelunya. Jangan jadi Jahat loh yaa!!

---
[⬅️ Sebelumnya: Error Menangkap Log](../08-Error-Handling/README.md) | [Lanjut ke Virtual Env (Level Up Dewa) ➡️](../10-Virtual-Env/README.md) | [🏠 Daftar Isi](../README.md)
