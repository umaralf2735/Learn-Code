# 03 - Array dan Hash di Ruby

Bahasa manapun butuh cara menyusun sekumpulan data, namun di Ruby sintaksnya jauh banget lebih luwes.

## 1. Array

Sama persis seperti JS, array tidak peduli kamu masukin apa kedalamnya (bisa campur), ukurannya pun melar sedirinya gaperlu repot.

```ruby
# Definisi array campur
kotak = ["Apel", 100, true]

# Cara tambah ke paling belakang di Ruby biasanya ga pakai 'append'/'push'
# Tapi pakai operator sekop (shovel) '<<' !!
kotak << "Semangka"

puts kotak[0] # => "Apel"

# Menghitung isi lemarinya
puts kotak.length # => 4
puts kotak.empty? # => false
```

### Rahasia Perulangan Array: `.each`
Selalu selalu selalu gunakan `.each` untuk memutar Array di Ruby. Ini budaya wajibnya:

```ruby
buah = ["Mangga", "Jeruk", "Pisang"]

buah.each do |nama_buah|
  puts "Saya mau makan #{nama_buah}"
end
```

## 2. Hash (Kamus / Map / Dictionaries)

Kalau di JS namanya Object, di sini sebutannya **Hash**. Hash itu adalah kunci dan lubangnya (Key & Value).

```ruby
# Hash lama:
# orang = { "nama" => "Bambang", "umur" => 30 }

# Hash Zaman Beradab (Ruby baru), 
# pakai 'Symbol' (tanda titik dua di depan). Super cepat di memori!
orang = { 
  nama: "Rizky", 
  umur: 24, 
  pekerjaan: "Programmer" 
}

# Ngambil datanya pakai tanda titik dua di belakang lagi
puts orang[:nama]
puts orang[:pekerjaan]

# Nambahin kunci baru
orang[:domisili] = "Depok"

puts orang
```

---
[⬅️ Sebelumnya: Struktur Kontrol](../02-Struktur-Kontrol/README.md) | [Lanjut ke Metode dan Blok ➡️](../04-Metode-dan-Blok/README.md) | [🏠 Daftar Isi](../README.md)
