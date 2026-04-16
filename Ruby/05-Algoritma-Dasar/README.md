# 05 - Algoritma Dasar Sakti (*Enumerable*)

Ini alasan Startup Web Amerika thn 2012an nyari Ruby Dev gede gedean gajinya! **ENUMERABLE**.
Lo gak perlu algrotime Looping For-while gak jelas untuk misain data. Ruby punya blok ajaib!

## 1. Perputaran `.each` (Sang Pengganti LOOP FOR)

Cukup Pake `.each do |variableSementara|`. Loop For klasik bakal kalah saing!

```ruby
karyawanPabrik = ["Robby", "Ganteng", "Makmur"]

karyawanPabrik.each do |orang|
    puts "Anak ini namanya: #{orang}"
end
```

## 2. Memetakan Array Baru `.map`
Sama kaya JS persis!! Ngubah smeua isi data mentah 1-1 dikali 2, lalu dilempar jadi Array Baru!

```ruby
isiDebit = [500, 10, 50, 2]

# Bikin langsung Array baru!! 
uangMeledakMega = isiDebit.map do |ongkok|
    ongkok * 1000  # Inget otomatis return Ruby
end

puts uangMeledakMega.inspect # Print mode Array asli
```

## 3. Hakim Pemilah Data `.select` (Sama dengan Filter di JS)

Misal ada ratusan data, lo mau nangkep Orang berumur di atas 18 tau buat dpilih jadi pemilih! Atau mencari angka genap doang:

```ruby
nomorSakti = [1, 5, 2, 8, 10, 99, 11]

ganjilanDoankNih = nomorSakti.select do |n|
    n.even?  # ADA FUNGSI BAWAANN NAMANYA (.even?) Nanya: Apakah genap?
end

puts ganjilanDoankNih.inspect # Output -> [2, 8, 10]
```

Ini adalah kempuan pamungkas dari `ActiveRecord Rails` untuk menyaring Ratusan Ribu baris  Database tnpa membebani Server lo.
---
[⬅️ Sebelumnya](../04-Metode-dan-Blok/README.md) | [Lanjut ➡️](../06-OOP-Class/README.md) | [🏠 Daftar Isi](../README.md)
