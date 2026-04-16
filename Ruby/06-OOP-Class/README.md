# 06 - Pemrograman Berorientasi Objek (Class)

Class itu ibarat cetakan / blueprint. Objek itu hasil kuenya! Karena di Ruby semuanya terbuat dari Objek, maka menguasai desain Class adalah harga terpenting di bahasa ini.

## 1. Membuat Blueprint dan InisialisasiAwal

Ketika kita mencetak kue dari sebuah cetakan (membuat Object class baru berdasar `.new`), maka metode bernama spesial `initialize` akan dipanggil otomatis pertama kali.

```ruby
class Mobil
  # Initialize: yang langsung dijalankan waktu dipanggil .new
  def initialize(merek, warna)
    
    # '@' (Instance Variable): Artinya dia variabel khusus milik cetakannya,
    # Ngga gampang ilang sekalinya metode ini selesai.
    @brand = merek  
    @color = warna
  end

  def cek_info
    puts "Saya bosan tapi saya punya mobil #{@brand} berwarna #{@color}"
  end
end

# Mari cetak objeknya!
mobil_saya = Mobil.new("Toyota", "Merah")
mobil_saya.cek_info 
```

## 2. Membaca dan Menulis Variabel dari Luar (`attr_accessor`)

Gawat! Di Ruby, kita sangat dijaga ketat. Kamu **TIDAK BISA MENGAMBIL @brand di luar method!**
```ruby
# puts mobil_saya.brand -> BAKAL ERROR BERDARAH!
```

Terus cara ngambilnya gimana? Kamu bisa tulis manual getter dan setternya, ATAU gunakan jurus rahasia Ruby: `attr_accessor` (Attribute Accessor).

```ruby
class Pemain
  # Memberikan akses baca dan edit dari luar!
  attr_accessor :nama, :nyawa

  def initialize(nama_hero)
    @nama = nama_hero
    @nyawa = 100 # Standar nyawa defaultnya 100
  end
end

hero1 = Pemain.new("Gatotkaca")

# Sekarang dari luar bisa di akses!!
puts "Darah si #{hero1.nama} sisa: #{hero1.nyawa}"

# Bisa di ubah pula!
hero1.nyawa -= 10
puts "Darah si #{hero1.nama} sekarat sisa: #{hero1.nyawa}"
```

Sangat rapi dan aman bukan desain OOP Ruby ini?

---
[⬅️ Sebelumnya: Algoritma Dasar](../05-Algoritma-Dasar/README.md) | [Lanjut ke Modul dan Mixin ➡️](../07-Modul-dan-Mixin/README.md) | [🏠 Daftar Isi](../README.md)
