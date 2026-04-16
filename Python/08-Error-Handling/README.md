# 08 - Menangani Kesalahan Program (`try...except`)

Tidak ada kata panik saat Python menendangmu dengan error marah-marah warna merah meluber muntah di Terminal. 

Masalahnya, begitu ada tulisan merah (*Exception/Crash*). Program Python kamu MATI TOTAL MENDADAK dan SEMUA SISA BARIS DI BAWAHNYA TIDAK AKAN KESENTUH DIBACA!! 

Ini bahaya parah kalo lu lagi jalanin Python d Server yg buka 24 jam. Makanya kita pake tameng pelindung maut: **Try..Except**.

## Pasang Sabuk Pengaman!

Bungkus hal ghaib mematikan kedalam try. Contoh terkuatnya adalah kamu mencoba menyatukan String dengan perhitugan Int (Ingat Javascript malah menjumlahkan text dan string secara ngasal kan menjuadi "101"? Tapi klo Python, dia Benci dan Lgsg ERROR NGAMUK!).

```python
print("Misi NASA Dimulai, Roket Naik...")

try:
    print("Mengeksekusi perhitungan satelit...")
    
    # ❌ KESALAHAN FATAL: Membagi dengan angka 0 ! (BISA MENGHANCURKAN MESIN PC)
    # ATAU Kesalahan ngetik Tipe Data Int ama STR digabungin murni jd + .
    pembagian = 10 / 0 
    
    # --- BARIS INI GABKAL KEPANGGIL Tembus!! Karena KEBIRU MELEDAK di baris hitungan nol td!
    print("Misi Selesai!") 

# --- JARING SPESIFIK PENANGKAP BOM TERSANGKA --- 

except ZeroDivisionError:
    # Error Spesifik yg kamu tembak target sasarannya! Mesin PC selamat.
    print("Woi, mana bisa angka di bagi sama nol!! Dasar payah, tapi untung aku tangkap.")
    
except Exception as curhatanErrorDunia:
    # Error Sapu Jagat (Apapun Error nya yg belum ke dftar jenis ditangkap jaring gede ini)
    print("Aduh ada error nih bosqueee gtau pokoknya error:")
    print("Pesan mesin PC asli: ", curhatanErrorDunia)
    
finally:
    # WAJIB SELALI DISEMATKAN DI BELAKANG Try Catch:
    print("-- Pembersihan Alat Mesin dan Koneksi Tutup Listrik. Entah dia meledak atau ngga, ini harus jalan. --")


print("ALHAMMULILAH MESKIPUN MELEDAK TAPI ROKET GAK MATI, BARI SINI MASIH TERCETAK")
```

Dengan ilmu `except`, pythonmu akan kebal dr bug-bug ketidaksengajaan input text dr User iseng (Form HTML) tanpa bikin PC server lu Force-Close Shutdown !!

---
[⬅️ Sebelumnya: Import Modul PIP](../07-Modul-dan-Pip/README.md) | [Lanjut ke File IO Tulis Tulis ➡️](../09-File-IO/README.md) | [🏠 Daftar Isi](../README.md)
