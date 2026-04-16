# 06 - Pemrograman Berbasis Konsep Objek Klasik (Ruby Class)

Meskipun segala nomor angka di Ruby itu sebenarnya murni *Object*. Lu gakkan bisa membangun *Arsitektur Server Aplikasi Web Raksasa* kalau gajbisa mendirikan blueprint `class` buatanu sendiori. Mari Kita Buat Cetakan Manusia!

## 1. Merakit Cetakan Baru & Jeroan `initialize` (Constructor)

Kalau JS pake `constructor`. Ruby Make embel emebl inisiasi yaitu: **`initialize`**.

```ruby
class MonsterRaksasa
    # Gerbang Yg pertama kali kepmanggil saaat dia kelar lahir  di cetak didunia! 
    def initialize(namaBocah, lvlDarahMulai)
        # 🌟 ILMU MAGIC @ (At Variabel Instance) 🌟
        # Biar namanya gak ilang begitu aja, kita Tancapin/Suntikin namanya tempel ke DALEM TUBUH ORGAN PRIBADINYA DIA SENDIRI pakai Huruf @ !!! (Ini Sm perss ky 'this.namaBocah' JS!!)
        @namaPanggilanBdnPribd = namaBocah
        @darahFullBadan = lvlDarahMulai
    end
    
    
    # Method Aktif Yg bsa di panggul
    def jurusNafasApiBau()
        puts "Wraaaaaaargghhhhh!!! Bakarr.. by #{@namaPanggilanBdnPribd}"
    end
end
```


## 2. Mencetak Objeknya Pake Sifat Gaib `.new`

Jangan ketik tulisan *new* kek dibahasa luarn ya di depam! Ruby itu memanggil New itu selayaknya elo Manghgil method method biasa wkwkwk! Gini loj carnyA:

```ruby
# LOH NEW NYA DITARUH DIBELKANG NMA CLASS?? IYAAAA!!! Bnerbener kaya method kan wkwkwk!!
bosTrukMaut = MonsterRaksasa.new("Optmius Hancr", 500000)

# Nah si Truk udh iddup brnafas!! Tnggal pgginl kkuatam ya! 
bosTrukMaut.jurusNafasApiBau()
```

Kalo kalian udah jago bikin ginian. Entar di RubyOnRails (RoR). Kalian tinggal narik data Model  kek gni : `User.new(:nama=> "Budi")` di simpen lalu di tmbak `User.save!`. Nanti Rails bkal otomatis Nulis Query `INSET INTO user` DB SQL dr belakang layar. Canggih bnget kn !

---
[⬅️ Sebelumnya: Enumbersble Array Modif](../05-Algoritma-Dasar/README.md) | [Lanjut ke Membajak Turunan (Mixin Modules) ➡️](../07-Modul-dan-Mixin/README.md) | [🏠 Daftar Isi](../README.md)
