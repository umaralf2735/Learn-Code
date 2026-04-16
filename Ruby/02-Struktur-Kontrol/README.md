# 02 - Struktur Kontrol dan Perulangan (Ruby Style!)

Logika `if` di Ruby ditutup dengan kata ganti `end` (Bukan pakai `{}` layaknya bahasa pemograman umum).

## 1. If / Elsif / Else

Penulisan standar untuk mengecek suatu kondisi : 

```ruby
nilai = 85

if nilai >= 90
  puts "Sangat Memuaskan!"
elsif nilai >= 75
  puts "Lulus!"
else
  puts "Uji perbaikan (Remedial)."
end
```

### Statement satu baris (Mantap!)
Kalau yang kamu suruh cuma pendek, kamu bisa mundurin posisinya ke belakang :
```ruby
uang = 1000

# Bakal cetak "Lapar" KALAU uangnya kurang dari 5000
puts "Lapar" if uang < 5000 
```

## 2. Keyword *UNLESS* (Kecuali Kalau)

Ruby punya keyword unik bahasa Inggris: `unless`. Ini sama aja kayak nulis `if tidak / if !=`. Buat yang malas pakai tanda seru `!`.

```ruby
apakah_hujan = false

# Bacanya: Jalan-jalan ke taman KECUALI KALAU hujan. 
puts "Jalan-jalan ke taman" unless apakah_hujan
```

## 3. Perulangan Ruby yang Super Elegan

Jujur saja, di Ruby orang SANGAT JARANG menggunakan `for i=0; i<x; i++`. Kenapa? Karena kita punya bahasa yang lebih natural.

### `.times` (Ulang sekian kali aja)
```ruby
5.times do |i|
  puts "Ayo semangat yang ke-#{i} kalinya!"
end
# Catatan: nilai `i` selalu dimulai dari angka 0, bukan 1.
```

### `while` standar
```ruby
baterai = 3

while baterai > 0
  puts "Senter Menyala!"
  baterai -= 1 # Kurangi 1
end

puts "Senter Mati."
```

---
[⬅️ Sebelumnya: Dasar-Dasar](../01-Dasar-Dasar/README.md) | [Lanjut ke Array dan Hash ➡️](../03-Array-dan-Hash/README.md) | [🏠 Daftar Isi](../README.md)
