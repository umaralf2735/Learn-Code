# 08 - Menangani Kesalahan Program (Try-Except)

Tidak ada kata panik saat Python menendangmu dengan error marah-marah warna merahnya di Terminal. Karena ada sabuk penganam yaitu **Try...Except**.

## Pasang Sabuk Pengaman!

Bungkus hal mematikan kedalam try. Contoh terkuatnya adalah kamu mencoba menyatukan String dengan perhitugan Int, dimana Python ga mentolelir hal ga masuk akal kayak Javascript (Javascript malah menjumlahkan text dan string secara ngasal kan?)

```python
try:
    print("Mengeksekusi misi...")
    
    # KESALAHAN FATAL: Membagi dengan angka 0 !
    pembagian = 10 / 0 
    
    print("Misi Selesai!") # Ini ga bakalan kepanggil

except ZeroDivisionError:
    # Error Spesifik yg kamu tembak target sasarannya!
    print("Woi, mana bisa angka di bagi sama nol!! Dasar payah.")
    
except Exception as p:
    # Error Sapu Jagat (Apapun Error nya ketangkap di sini)
    print("Aduh ada error nih bosqueee:")
    print(p)
finally:
    print("-- Pembersihan alat mesin beres meskipun terjadi ledakan --")
```

Dengan `except`, Pythonmu akan tetap berlari menjalankan baris ke bawahnya tanpa mengamok langsung menghentikan paksa *software* yang sudah susah-susah kalian bagun.

---
[⬅️ Sebelumnya: Modul dan Pip](../07-Modul-dan-Pip/README.md) | [Lanjut ke File IO ➡️](../09-File-IO/README.md) | [🏠 Daftar Isi](../README.md)
