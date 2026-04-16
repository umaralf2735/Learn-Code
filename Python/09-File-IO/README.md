# 09 - Bermain Mengobrak-Abrik Berkas Teks (File I/O)

Membongkar File dengan python itu sangat sakti dan ga konyol-konyol bocornya kayak di bahasa C sana. Sama seperti Ruby yang pemaaf, begitupun Python.

## Pintu Gaib Bernama `with open`

Rahasia aman dari membongkar file `.txt` atau apapun biar komputermu memorinya gak bocor saat kalian "Lupa nge-Close" filenya adalah pakai metode modern `with`.

```python
# Tulis dan Timpa isi Teks ("w" berarti WRITE)
# Kalau ga mau nimpa dan pengen sambung ke bawah, pakailah ("a" atau APPEND)
with open("data_sakti.txt", mode="w") as file_ku:
    file_ku.write("Ini adalah teks baris pertama!\n")
    file_ku.write("Aku berhasil nyimpan ini diam diam!!")
    # PERHATIKAN: setelah blok ini menjorong ke kiri lagi, file otomatis DITUTUP SENDIRi!


# Cara Membacanya sangat simple: Mode "r" (READ)
with open("data_sakti.txt", mode="r") as bukuku:
    semua_text = bukuku.read()
    print("Isi bukunya:")
    print(semua_text)
```

Dengan ilmu file IO ini, para H4ck3r python biasanya menyimpanni log sandi bajakan orang lain menggunakan `append ("a")` supaya laporannya memanjang permanen di Harddisknya diam-diam!

---
[⬅️ Sebelumnya: Error Handling](../08-Error-Handling/README.md) | [Lanjut ke Virtual Env ➡️](../10-Virtual-Env/README.md) | [🏠 Daftar Isi](../README.md)
