# 07 - Modul Penyelamat Hidup (Mixins Anti Pewarisan Tunggal)

Kalian mau bikin game.  Ada Musuh *Bos Naga Terbang* dan ada Hero *Babat Bebek Terbang*!.

Kebanyaan Bahasa itu cuman ngebolehin PEWARISAN (`extends / < ` Inheritance Class Bapak Anak) itu CUMAN SATU doankkk.. Nah misla lo bikin Bapak Class "MakhulukTerbng". Nnti si bBEK sm NAGA nya bs terbang... 

Tapiii gimna crny  ngash mreka kemampuan "Mengeluarkan Api DiMulut??" Mnsa lu bkin class induik br dgan nam MahaklukTEranngYgBSKluarainAPi??? Pusing wkwk!!.

Ruby dtang mnbyelkstnmasalah Make **`module`**!! (Cuma sekumpulan sipat saku yg is dselipin kesiapapun!!/  MIXIN).

## 1. Nyimpen Modul Sifat Saku
```ruby
# Ini bkan class, ini cmn sifat ngambang aja
module KemampuanBerterbanHampaUdara
    def kepakanSayapBesi()
        puts "Zwwwuuuuungggg.... Nggangkat bdna k ats langit..."
    end
end

module KemampuanBuangApiDariMulut
    def bakarAreaDpanMata()
       puts "Fwhooooosshhhh!! Kepnjnasann bosu!" 
    end
end
```

## 2. MENANCAPKAN SIFAT (Include Mixin!)

Ini dia enaknya RubY!!! Lo bisa masukin *Dua Module itu sklaigus* dan nbikin Class lu jago dan Pnya kkuatan mrk brdua scr Instan murni!!! 

```ruby
class NagaPutihMataBiru
    # 🌟 SELIPPIN SIFAT ALIEN NYAAAA PAKE INCLUDE!!
    include KemampuanBerterbanHampaUdara
    include KemampuanBuangApiDariMulut
    
    def initialize(namanya)
       @namanya = namanya 
    end
end

# TEsting mnyala!
nagaGueeeSeketikaIddupp = NagaPutihMataBiru.new("Cihuy Raksassasa")

# WAH ALHAMUDILALH... CLASSS NAGA NYA TIBA TIB PUNYA SKILL YFG ADA DI MODULE!! GAUSAH REPOT REPOT NURUNIN DARI CLASS BPK!!
nagaGueeeSeketikaIddupp.kepakanSayapBesi()
nagaGueeeSeketikaIddupp.bakarAreaDpanMata()
```

Luar biasasa Ruby ini. Sifat `Module Include` di ruby inilah yang memebrikan insepiraasi kpada bhsa modern utk nyiptatin Fitur "Traits" spti di PHP dan Rst Language lho!!

---
[⬅️ Sebelumnya: Class Object Mewah](../06-OOP-Class/README.md) | [Lanjut ke Kurungan Begin Error Rescue ➡️](../08-Error-Handling/README.md) | [🏠 Daftar Isi](../README.md)
