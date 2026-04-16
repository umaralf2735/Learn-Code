# 04 - Metode (Method) dan Blok (Block)

## 1. Metode (`def`)

Metode di Ruby sangat magis. Kita mendefinisikannya dengan keyword `def`...`end`.

Dan tahukah kamu bagian terkerennya? **Kamu tidak perlu nulis "return"!** Ruby secara otomatis akan menganggap baris terakhir dari sebuah metode sebagai hasil yang dikembalikan.

```ruby
# Membuat Metode
def hitung_perkalian(a, b)
  hasil = a * b
  hasil # ini baris terakhir, otomatis jadi nilai yang dikembalikan (return)
end

# Memanggilnya
angka = hitung_perkalian(5, 4)
puts "Hasil: #{angka}"
```

Ajaibnya lagi, kalau parameternya jelas, kamu gak perlu nulis tanda kurung loh saat memanggil!
```ruby
def sapa_orang(nama)
  puts "Halo, #{nama}!"
end

# Lebih natural dibaca!
sapa_orang "Raditya" 
```

## 2. Blok dan `yield` (Nyawa aslinya Ruby)

Blok adalah serpihan kode yang dikepung oleh `do ... end`. Ini sering banget diculik sama Method untuk dijalanin. Method menggunakan keyword `yield` untuk mengeksekusi blok!

```ruby
def panggil_blok_dong
  puts "1. Method dimulai"
  
  yield # DI SINI METHOD TERJEDA, DIA MELEMPAR EKSEKUSI KE BLOK DI BAWAH

  puts "3. Kembali ke dalam Method dan Selesai!"
end

# Kita panggil methodnya, sekalian kita sumpal pakai blok kode:
panggil_blok_dong do
  puts "2. (Ini tulisan blok yang disisipkan!)"
end

# Output: 
# 1. Method dimulai
# 2. (Ini tulisan blok yang disisipkan!)
# 3. Kembali ke dalam Method dan Selesai!
```

Konsep `yield` dan blok inilah yang akan sangat amat sering kamu temui di Framework Ruby on Rails!

---
[⬅️ Sebelumnya: Array dan Hash](../03-Array-dan-Hash/README.md) | [Lanjut ke Algoritma Enumerable ➡️](../05-Algoritma-Dasar/README.md) | [🏠 Daftar Isi](../README.md)
