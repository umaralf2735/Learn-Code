# 03 - Penyimpanan Sekardus (Array & Hash Symbols)

Gak nendang kita gabisa manipulasi Banyak data orang sekaligus kalau ga ada Array. Di Ruby, fitur maut ada pada Dictionary / Object Json nya yang dinamakan sebagai `Hash`!

## 1. Array Dinamis 

Kaya Python. Array nya Ruby ga usah dipesen brapa ukuran dan tipe datanya. Bebas dan sangat luwes.

```ruby
lokerBarang = ["Pistol Kayu", "Garam", 99, false]

# Nambah pake PUSH biasa (Ujung kanan)
lokerBarang.push("Botol Air")

# MENGAKSES NYA PAKE INDEX BIASA
puts "Senjata petama saya adlah: #{lokerBarang[0]}"

# ALAT PISAU DEWA RUBY! Punya alias Bahasa Inggris ghaib:
puts "Ujung DEPAN : #{lokerBarang.first}"
puts "Ujung BLAKNG: #{lokerBarang.last}"
```

## 2. Hash & Symbols (Objek JSON nya Ruby)

Di PHP dinamain Array Assosiatif. Di Python ini sebutannya Dictionary. Inilah Hash. Punya Kunci Teks (Key : Value) berpasangan dlam Kurawal `{}`.

Di Ruby, untuk mengirit RAM Supaya **Kuncinya GAK DICOPY BERKALIKALI JADI STRING**, mereka nyiptain yang namanya `SIMBOL (Tanda Titik dua `:namakunci`)!!` Ini lbih enteng drpd string "namakunci" biasa!

```ruby
# Nyetak Object Json
bukuRekamMedis = {
    :namaPasien => "Bang Toyib",
    :riwayatSakit => "Masuk Angin",
    :umur       => 45
}

# NGAMBILNYA LU HARUS PANGGIL 'ALAT TUKAR' SIMBOLNYA:
puts "Dokter tolong periksa bapak #{bukuRekamMedis[:namaPasien]}"

```

**TRICK PENULISAN DEWA JS STYLE:**
Kalau capek nulis Panah `=>` gemuk gitu kek PHP. Kalian BOLEH nulis gaya Javascript. Taruh titik duanya ke samping kanan! 

```ruby
# INI LBH RINGKAS KEK JAVASCRIPT! LBH CAKEP!
bukuBaru = {
    namaPasien: "Ridho Ilahi",
    umur: 20
}

puts "Siang bang #{bukuBaru[:namaPasien]}" # NAMUN NGAMBILNYA TETAP PAKE SIMBOL TITIK DUA KIRI YA!
```
---
[⬅️ Sebelumnya](../02-Struktur-Kontrol/README.md) | [Lanjut ➡️](../04-Metode-dan-Blok/README.md) | [🏠 Daftar Isi](../README.md)
