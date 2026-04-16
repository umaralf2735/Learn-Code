# 10 - Memungut Harta Karun Semesta (RubyGems & Bundler)

Sebagai seprang programmer ruby yg handal... Apakah kalian akan mendevelop fitur Kirim Emain OTP lwat GMAIL itu secera manual dari 0?? 
Jangan menciptakan roda lagi klo rodanya uda dibikinin orang hebat di internet! 

Sama seperti JavaScript dengan Node Modules (NPM) dan Python dengan PIP nya. Ruby juga punya gudang pustaka dunia yang disebut: **GEMS**.

## 1. Nyedot Menginstall Gem ke Komputer
Pastikan uda install ruby d CMD termnal. Misal lo pengen nyari pustaka buat mewarnai Teks di Terminal Lu biar ga putih hitam mlu. Namanya Gem `colorize`.

Ngedownloadnya tinggal ketik : 
```bash
gem install colorize
```

## 2. Memakainya di Dalam Script Ruby 

Buka file ruby biasa. Tarik nama gem nya pake mantra dewa `require` bwat masukin modulnya!

```ruby
# Narook di praling atas biar dsedot semua 
require 'colorize'

# TIBAA TIBAAAA!!!
# STRING Biasamu mempunyai sakti methods baru namanya color !!
puts "Awas ada polisi di depan brroo !! ".colorize(:red)

puts "Santai aja cuy kita bawa stnk kkok ".colorize(:green)
```


## 3. Sang Pengatur Proyek Besar (Bundler & Gemfile)

Kolo proyek lo makin gede trus butuh ratusan GEM dalm waktu brsamaan.. Masa lu nyuruh temen tim lu ngetikin `gem install xxx` ratusan kli di PC mereka? 

Gausaa!! Kita bbuat file resep canggih Mnamanya `Gemfile`.

```ruby
source 'https://rubygems.org'

# Gua tlis gem apa aja dsnini!
gem 'colorize'

# Ini dia framework sakti yg membuat ruby tetap menyala hingga detik ini!!
gem 'rails', '~> 7.0.0' 
```

Trus di cmd terminal lo.. ketik mantra ini baut nginstal massal murni tanpa nyentuh file satupun!!
```bash
bundle install
```

# TAMAT! KELAR!
Kalian sudah meRngausai sintaks dasar bahasa RUBY yang mendunia ini! Langkah lanjutan adalah kalian mencoba framework backend API yang sangat disukai perusahaan startus amerika yaitu **Ruby on Rails (RoR)** !! Selamat ngoding!

---
[⬅️ Sebelumnya](../09-File-IO/README.md) | [🏠 Daftar Isi Utama](../README.md)
