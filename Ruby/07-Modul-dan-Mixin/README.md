# 07 - Modul Penyelamat Hidup (Mixins Anti Pewarisan Tunggal)

Kalian mau bikin game. Ada Musuh *Bos Naga Terbang* dan ada Hero *Bebek Terbang*!.

Kebanyakan Bahasa itu cuman ngebolehin PEWARISAN (Inheritance Class Bapak Anak) itu CUMAN SATU doang. 
Ruby datang menyelesaikan masalah tumpang tindih ini dengan **`module`**!! (Cuma sekumpulan sifat saku yg is diselipin kesiapapun!!/ MIXIN).

## 1. Nyimpen Modul Sifat Saku
```ruby
# Ini bukan class, ini cmn sifat ngambang aja
module KemampuanBerterbang
    def kepakanSayap()
        puts "Zwwwuuuuungggg.... Melayang ke langit"
    end
end

module KemampuanBuangApi
    def bakarAreaDpanMata()
       puts "Fwhooooosshhhh!! Kepnjnasann bosu!" 
    end
end
```

## 2. MENANCAPKAN SIFAT (Include Mixin!)

Lo bisa masukin *Dua Module itu sekaligus* dan bikin Class lu jago dan Punya kekuatan gabungan secara instan!

```ruby
class NagaPutihMataBiru
    # SELIPPIN SIFAT ALIEN NYAAAA PAKE INCLUDE!!
    include KemampuanBerterbang
    include KemampuanBuangApi
    
    def initialize(namanya)
       @namanya = namanya 
    end
end

# Testing menyala!
nagaGue = NagaPutihMataBiru.new("Shiro")

nagaGue.kepakanSayap()
nagaGue.bakarAreaDpanMata()
```

Luar biasa Ruby ini. Sifat `Module Include` di ruby inilah yang memberikan inspirasi pada bahasa modern utk menciptaan Fitur "Traits" spti di PHP dan Rust Language lho!!
---
[⬅️ Sebelumnya](../06-OOP-Class/README.md) | [Lanjut ➡️](../08-Error-Handling/README.md) | [🏠 Daftar Isi](../README.md)
