# 05 - Algoritma Dasar (Enumerable Magic)

Sama seperti JavaScript, kita jarang nulis Bubble Sort manual di Ruby, karena Ruby memiliki pustaka sakti bernama **Enumerable**. (Inilah kenapa `do...end` sebelumnya dipelajari).

## 1. Searching (Penyaringan dan Pencarian)

Mau menyaring data siswa yang nilainya diatas 75? Tak perlu looping manual, pake bajak laut `.select` (atau filter).

```ruby
nilai_ujian = [60, 80, 45, 95, 78]

# Cukup 1 baris, suruh Ruby nyeleksi (select)
yang_lulus = nilai_ujian.select do |n| 
  n > 75 
end

puts "Siswa lulus: #{yang_lulus}" # => [80, 95, 78]
```

Atau kalau hanya mau mencari **satu** orang saja? Pakai `.find`

```ruby
angka_dicari = nilai_ujian.find do |n| 
  n == 95 
end
```

## 2. Mengubah Format Data (.map)

Ini algoritma keren kalau kamu mau memodifikasi semua isi array tapi disimpan ke dalam bentuk kotak (Array) baru!

```ruby
daftar_harga = [100, 200, 500]

# Tolong dong harga-harga diatas dikali 2 buat bayar ongkir!
ongkir = daftar_harga.map do |bayar|
  bayar * 2
end

puts "Biaya aslinya: #{daftar_harga}" # => [100, 200, 500]
puts "Daftar bayar ongkir: #{ongkir}" # => [200, 400, 1000]
```

## 3. Sorting (Mengurutkan)

Otomatis naik kecil-kritis? Kasih aja `.sort!`

```ruby
abjad = ["Z", "A", "M", "B"]

# Urutkan abjadnya!
abjad_terurut = abjad.sort

puts abjad_terurut # => A B M Z
```

Intinya di Ruby, kalau bisa diselesaikan dengan ngomong berbahasa Inggris 1 baris, ngga perlu dibikin ribet berpuluh-puluh baris kawan!

---
[⬅️ Sebelumnya: Metode dan Blok](../04-Metode-dan-Blok/README.md) | [Lanjut ke Pemrograman Class ➡️](../06-OOP-Class/README.md) | [🏠 Daftar Isi](../README.md)
