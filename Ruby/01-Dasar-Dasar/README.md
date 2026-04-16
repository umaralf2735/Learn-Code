# 01 - Dasar-Dasar Ruby

Menulis Ruby terasa seperti menulis puisi berbahasa Inggris! Mari kita lihat mengapa Ruby dinobatkan sebagai bahasa paling *friendly* abad ini.

## 1. Menampilkan Output ke Layar

Bila Golang punya `fmt.Println` dan JS punya `console.log`, Ruby jauh lebih sederhana:

```ruby
# Puts (Put String) - Mencetak tulisan lalu MENAMBAH garis baru kawan (Enter)
puts "Halo dunia, ini pakai puts!"

# Print - Mencetak tulisan TANPA menambah garis baru di akhirnya
print "Saya suka "
print "makan nasi goreng.\n" # \n secara manual turun enter
```

## 2. Variabel tanpa embel-embel

Kamu tidak perlu menulis tipe data, tidak perlu juga nulis `var`, `let`, apalagi titik koma (`;`) di akhir baris. Cukup sebutkan dan isi!

```ruby
nama_saya = "Budi Santoso"
umur = 22
sedang_belajar = true

puts "Nama saya adalah #{nama_saya} dan umur saya #{umur}."
# Note: '#{...}' digunakan untuk memasukkan isi variabel ke dalam sebuah teks, 
# SYARATNYA: harus pakai petik ganda ganda ("..."), gak nge-efek kalau petik satu ('...').
```

## 3. "Everything is an Object" (Segalanya adalah Objek)

Di bahasa lain (seperti Java atau Golang), angka `1` atau teks `"Halo"` itu cuma data mentah (Primitf). Di Ruby, angka, string, true/false, BAHKAN nilai kosong (Nil/Null) itu adalah benda (Objek) hidup yang punya fungsinya (Methods) masing-masing!

```ruby
# Lihat betapa gilanya Ruby terhadap metode bawaan
puts "Budi".upcase           # => "BUDI"
puts "malam".reverse         # => "malam" (dibalik jadi "malam")
puts -5.abs                  # => 5 (Nilai absolut)
puts 3.even?                 # => false (Apakah 3 angka genap?)

# Karena nil itu adalah objek di Ruby (bukan udara kosong),
# Kita bisa tanya: Apakah kamu kosong? 
puts nil.nil?  # => true
```

---
[Lanjut ke Struktur Kontrol ➡️](../02-Struktur-Kontrol/README.md) | [🏠 Daftar Isi](../README.md)
