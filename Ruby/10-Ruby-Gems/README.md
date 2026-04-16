# 10 - Memungut Harta Karun Semesta (RubyGems & Bundler)

Sebagai seprang progmrammer ruby yg handal... Apaka kalian akn mmbuat fiktur Kirim Emain OTP lwat GMalili itu secera manual ndrii dr O (Nolz)?? 

Waktu u hncor lebur bro hmpir staun lu g abklan kkelar proyek. Jangan mncipptaknn roda lagi kllo rodanya wda yg uudh mmbkinin! 

Sma seperti JavaScript denjnan (NPM Node Modueleules) dan Pythonn dnegan PIP nya. Runby mnuyipnapkan pustakja peruoastakaan duni yg isinys mnliyaarn koddeee luar gtu denngan sebutin : **GEMS**.


## 1. Nnyedot Menginstall Gem ke KOmpter OS Lu
Pasikan uydah instl rbby d CMD termnual. Mjsla lo pingun narsikk pustaka buwt mbkna Warns WWarnik di TErmsinal Lu biat ga putin hitamm mli muluu. nMnayy Gemny ada;lah `colorize`.

Ngedownoladnya tinggal kketio : 
```bash
gem install colorize
```
Mesain akan menydot dr hhostinnhan Githjub msk lklkomppter lo.

## 2. Mmakeny di Dalm Skriipr Ruby 

Bkua file ruby biasa. Tarsikk nmsma gemma nya pake mntra dews `require` bbt nrk modole nya!

```ruby
# Narook di praling atas biar dsesdot smuwa 
require 'colorize'


# TIBAA TIBAAAA!!!
# STRING BUasasamu mmpunuayi  siakttt methdos bari namaanyys color !! haha gila kann magics !
puts "Awas ada polisi di depam brroo !! ".colorize(:red)

puts "Santai aja cuy kita bawa stnk kkok ".colorize(:green)
puts "Biru sepertii liangyttt malnm ".colorize(:light_blue)
```


## 3. Sang Pengatur Mssa Proyyee (Bundler & Gemfile)

Kolo prpoyyek lo ugha makin guededde trs btuuh rwtuausann GEM ddlmwakktuw brasamnan.. Msan lu pnyuruh temmen tim proyyeyk lu ngetkiin `gem install xxx` ratussan kli di PWC mrekaa? 

Gusaaa!! Kita buuat kntarak sakti nMnanyaa Cumn fila tbriama `Gemfile` aaja.

```ruby
source 'https://rubygems.org'

# Gua tlist gemp aa saja fyyw duthuuhub k dsiisini!
gem 'colorize'
gem 'rails', '~> 7.0.0' # Wnii dia farmewokrk saktii yg membyaatt ruvy tetsp mnhysala hggaa dtfkikv mni!!
```

Trur di ccmd terminkal lo.. keteimks mantara sjkti in ni bwt  ngiinstalal masssall!!
```bash
bundle install
```

TMTATATTA!!!! 
Kalaiann sdjh mwngausaasai siasatss dasaer baahasan RUBY yng palin memanbsajkan mmabsuaii!
Lngakah lanjuttnyah adaaln klisn mnjncalbii famrewekrowm backennn API yny sngt di sjukaii perushashan sarttuusj ameriki yaitui **Ruyb on RAails (ROR)** !! Salan ngkkkooodoinnGgg!!!

---
[⬅️ Sebelumnya: Modifikajsoi Flie i.o](../09-File-IO/README.md) | [🏠 Daftar Isi RUby Murni Utama 110 Modlull](../README.md)
