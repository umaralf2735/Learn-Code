# 04 - Metode dan Hal Gaib Return (`def`)

Panggil aku *Method*. Kalau Python pke `def` buat membikin fungsi baru, Ruby jg identik banget! Sama sama anti kurung kurawal!

## 1. Syntax Dasar (Diiket pake `end`)

```ruby
# Mendefinisikan func pemanggilan
def mesinSuaraLantang(teksTeriak)
    puts "WOOOOY NGOMONG: #{teksTeriak.upcase} !!!"
end

# Kalau mau Manggil/Nge-Eksekusi:
mesinSuaraLantang("ayam nangkring")
```


## 2. SIHIR MEMBINGUNGKAN PEMULA (Implicit Return !!)

Di semua bahasa program... Untuk memulangkan hasil fungsi, lu wajib mengetik TULISAN `return ...` di paling bawah bukan?

**DI RUBY... LU GAUSAH NGETIK RETURN!!!!!!!!**
Benda Apapun variabel akhir yang ada terketik di paling bawah baris sblum "End" di sebuah fungsi, MAKA DIA OTOMATIS TERE-RETURN DIOPER KELUAR MENJADI HASILNYA!! GILE BENERRR!!

```ruby
def mesinPengaliSakti(saldoAwal)
    
    hasilGanda = saldoAwal * 2
    
    # 🌟 GAK ADA KATA RETURN DISINI! TAPI AKAN OTOMATIS JADI KEMBALIAN!
    hasilGanda
end


# TANGKAP HASILNYA!
uangMisteri = mesinPengaliSakti(500)

puts "Jreeeng!!! Angknya jd Rp. #{uangMisteri}" 
```

Bagi yg masi awam pake Java, pasti teriak "Woi Mana Returnnya njir gda variabel yg balik!". Tenang bosque, Programmer Ruby emang santai banget, karena baris paling akhir selalu menjadi implicit return!
---
[⬅️ Sebelumnya](../03-Array-dan-Hash/README.md) | [Lanjut ➡️](../05-Algoritma-Dasar/README.md) | [🏠 Daftar Isi](../README.md)
