# 06 - Pemrograman Berbasis Object (Ruby Class)

Meskipun segala nomor angka di Ruby itu sebenarnya murni *Object*. Lu gakkan bisa membangun *Arsitektur Server Aplikasi Web Raksasa* kalau gabisa mendirikan blueprint `class` buatanmu sendiri.

## 1. Merakit Cetakan Baru & Jeroan `initialize` (Constructor)

Kalau JS pake `constructor`. Ruby Make kata berlabel: **`initialize`**.

```ruby
class MonsterRaksasa
    
    // Gerbang yang pertama kali kepanggil
    def initialize(namaBocah, lvlDarahMulai)
        
        # ILMU MAGIC @ (At Variabel Instance) 
        # Biar namanya gak ilang begitu aja, kita Suntikin namanya ke DALEM TUBUH ORGAN PRIBADINYA DIA SENDIRI pakai Huruf @ !!! 
        # (Ini Sama persis kaya 'this.namaBocah' JS!!)
        
        @namaPanggilanPribadi = namaBocah
        @darahFullBadan = lvlDarahMulai
    end
    
    
    # Method Aktif
    def jurusNafasApi()
        puts "Wraaaaaaargghhhhh!!! #{@namaPanggilanPribadi} membakar seisi kota!!"
    end
end
```


## 2. Mencetak Objeknya Pake Sifat Gaib `.new`

Jangan ketik tulisan *new* kek dibahasa luarnya ya di depan variabel! Ruby itu memanggil New itu selayaknya elo Manggil method beneran!

```ruby
# Panggil dari belakang Nama Class nya:
bosNagaApi = MonsterRaksasa.new("SmaugSiNaga", 500000)

bosNagaApi.jurusNafasApi()
```

Kalo kalian udah jago bikin ginian, framework MVC canggih seperti Ruby on Rails bakal sangat gampang dimengerti luar dalem!
---
[⬅️ Sebelumnya](../05-Algoritma-Dasar/README.md) | [Lanjut ➡️](../07-Modul-dan-Mixin/README.md) | [🏠 Daftar Isi](../README.md)
