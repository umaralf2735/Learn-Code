# 10 - Menyedot RubyGems (Pemasok Otak Rails)

Apakah kamu penasaran darimana datangnya kemampuan Web raksasa sebuah *Framework Rails*? Semuanya dikemas dari sekumpulan perpustakaan gaib yang bernama **Gems**.

RubyGems adalah pasar gratis paket alatnya orang-orang Ruby Universe. Sama persis tabiat komuntasnya seperti Composer di PHP (Packagist). 

## 1. Instalasi Library

Lewat terminal CLI (Pastikan Ruby sudah terpasang global), kamu bebas menyebut nama paket apapun.
Contoh, kita ingin menginstall mesin pencetak uang kripto palsu / pembuat nama samaran sakti benama Faker.

```bash
gem install faker
```
Beres deh!

## 2. Bagaimana Manggil File Rahasianya?

Sesederhana melempar surat rayuan ke dalam `require`! (Kalau kamu pakenya Ruby tua)

```ruby
# Panggil bungkus Gem nya
require 'faker'

puts "Sebutkan nama palsu peretas!"
puts Faker::Name.name 
# Output dinamis tiap dipanggil: Dr. Oki Suryata 

puts "Cetak alamat boongan!"
puts Faker::Address.city
```

## 3. Bundler - Mengikat Koper Alat

Kalau mau merakit program yang ada 20 library `gems`, masa orang lain yang *download* PC kita disuruh nulis `gem install xx` dua puluh kali di terminal? Gila. Olenghingga, pakailah **Bundler**.

- Kamu bikin 1 resep koki ditext berformat `Gemfile`.
- Didalamnya ditulis:
```ruby
source 'https://rubygems.org'

gem 'faker'
gem 'rspec'
gem 'sqlite3'
```
- Orang yang nerima kode mu di Jepang, tinggal cuma buka terminal dan ngetik saktimandraguna: `bundle install`.

TARA!!! Semua dependensi 100% dipenuhi sendiri!

---
[⬅️ Sebelumnya: File I/O](../09-File-IO/README.md) | [🏠 Daftar Isi Utama](../README.md)
