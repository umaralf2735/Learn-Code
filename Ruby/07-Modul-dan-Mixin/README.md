# 07 - Modul dan Mixin

Bab terakhir dari pondasi Ruby adalah Module. Modul itu mirip sekali dengan Class, hanya saja punya pantangan: **kamu tidak bisa mencetak Objek baru (gitar.new) dari sebuah Module!**

Terus buat apa ada modul? Dia hadir untuk **Ngumpulin Method** yang bertemakan sama, biar nggak campur aduk di kerangka global.

## 1. Pembuatan Modul (Namespace)

Kamu punya 2 cara mencetak sapaan yang namanya mirip. Gampang! Masukin ke dalam folder Modul masing-masing.

```ruby
module SapaanRamah
  def self.pagi
    "Selamat Pagi Boskuuuhhhh"
  end
end

module SapaanGalak
  def self.pagi
    "Woi bangun lu pemalas!"
  end
end

# Karena mereka Modul beda folder, manggil fungsinya ga bakal bentrok:
puts SapaanRamah.pagi
puts SapaanGalak.pagi
```

## 2. Mixin (Mencampurkan)

Nah, ini dia jurus andalannya. Modul ini bisa ditempel / di-injek ke dalam Class buatan kamu menggunakan sakratul `include`. 

Ini persis jika kamu bermain Game: 
Hero kamu dari Class biasa-biasa aja, tiba-tiba ngambil Armor Terbang dari modul luar, langsung bisa sakti!

```ruby
module KemampuanTerbang
  def terbang
    "Akuuuuu Tttteeerrrrbanngggg!!! Wusssss!!"
  end
end

class Burung
  # Masukin Modul Terbannya (Diserap, di-include-kan)
  include KemampuanTerbang 
end

class Pesawat
  # Sama, pesat juga include!
  include KemampuanTerbang
end

class Kucing
  # Kucing tidak terbang, jadi gak usah masukin Modul Terbang
end

burungKu = Burung.new
puts burungKu.terbang # => Akuuuuu Tttteeerrrrbanngggg!!! Wusssss!!
```

Kalian nggak perlu bikin fungsi `terbang` berulang-ulang di burung dan pesawat. Cukup taro di Modul lalu *include* ! Sangat efisien dalam menata program raksasa (Ini sering terjadi di dalam Ruby on Rails Controllers!).

---
[⬅️ Sebelumnya: OOP Class](../06-OOP-Class/README.md) | [🏠 Daftar Isi Utama](../README.md)
