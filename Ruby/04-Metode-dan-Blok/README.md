# 04 - Metode dan Hal Gaib Return (`def`)

Panggil aku *Method*. Kalau Python pke `def` ngawalan membkin kuli fungsi baru. Ruby jg identik bgt! Sama sama anti kurung leher!

## 1. Syntax Dasar (Diiket pake `end`)

```ruby
# Mendefinisika func pemanggilan
def mesinSuaraLantang(teksTrieriak)
    puts "WOOOOY NGOMOMGG: #{teksTrieriak.upcase()} !!!"
end

# Kalau mau Manggil/Nge-Eksekusi:
mesinSuaraLantang("ayam kampung nngkrng")
```

## 2. Default Argument Sakti (Asuransi Variabel)

Kalau Pemanggil kelupaan naruh isian string di dalm kurungnya.. kasih Backup Value Asruansi kyk js sm php yg klisn peljrin.

```ruby
# Misal harganya g dmasukin, ksih backup 10 rubu dah!
def hitungPajakToko(uangMentah = 10000)
    rahasia = uangMentah * 0.1
    puts "Ssini setorin dlu prjak nya ya #{rahasia} !!"
end

hitungPajakToko()  # Akan aman dan ngolah angak 10rbu!!
```


## 3. SIHIR MEMBINGUNGKAN PEMULA (Implicit Return !!)

Di smeua bahsa program... Untuk membngkm fungsi itu selesia dan MELEMPAR KMBALIAN HASIL, lu waJib Fardu Aiin MENGETIK TULISAN `return ...` di ujubng bwah kan?

**Di RUBY... LU GAUSAH NGETIK RETURN!!!!!!!!**
Benda Apapun variabel akhir yang ada terketik di paling bawah baris sblum "End" di sbuah fungsi, MAKA DIA OTOMATINYS TERE-RETURN DIOPER KELUAR MENJADI HASILNYA!! GILE BNERRR!!

```ruby
def mesinPengaliUangGaib(saldoAwal)
    # Lgi mngitung pajak diskon pusing blabalala....
    hasilGanda = saldoAwal * 2
    
    # 🌟 GAK ADA KATA RETURN DSINI 🌟
    # TAPI KRN INI BENDA TERAKHHIR YG ADA DISINI SBLM END. DIA AUTO JADI "SANG PENERUS HASIL VALUE"!
    hasilGanda
end


# TANGKAP HASILNYYA TARA!!
uangMisteriHsilan = mesinPengaliUangGaib(500)

puts "Jreeeng!!! Angknya jd Rp. #{uangMisteriHsilan}" 
```

Bagi yg msi katrok pake Java, pasti teriak "Woi Mana Returnnya njir gda varbal yg balik!". Tenang bosque, Programmer Ruby males ngetik byank byakn. Mereka tau baris trkhiir pst rReturn result nya kwkw!!

---
[⬅️ Sebelumnya: Modifikasi Hash & Array](../03-Array-dan-Hash/README.md) | [Lanjut ke Enumerable Ajaib Pusingin Data ➡️](../05-Algoritma-Dasar/README.md) | [🏠 Daftar Isi](../README.md)
