# 02 - Struktur Kontrol (If, Else, dan Magis `unless`)

Mari kita bahas IF ELSE nya. Inget yg diawal kubilang, ngga ada Kurung Kurawal `{ }` pusing lagi. 
Sebagai gantinya. Kalian diwajibkan Mengunci gerbang Logikanya menggunakan kata mutlak **`end`** dibawahnnya!!

## 1. Percabangan dengan `if` dan `elsif`

Perhatikan! bukan Else If yak, TAPI disingkat menjadi **`elsif`**!!

```ruby
darahMusuh = 25

if darahMusuh >= 50
    puts "Maju teruss tank nya tebel bosque!"

elsif darahMusuh >= 15
    puts "Sikat udah Sekarat nanggung!"
    
else 
    puts "Hit sekali lagi mati!!!"
    
end # INI WAJIB! SBAGAI PENGGANTI KURUNG PENUTUP } MURNI!!
```

## 2. Sang Pelawan Arus Sakti (`unless`) 

Kalo di bahasa C lu nulis syarat tidak sama dengan kayak gini "Kalo GAK Ujan" : `if ( !hujanAman )`. Ngetik TANDA SERU `(!)` kadang suka keselip nyempil ga gampang diliat mata orang.

Ruby nyiptain kata *"KECUALI KALAU..."* (`unless`). 
**Dia bakal Njalanin bloknya KETIKA SYARATNYA BOHONG/FALSE!!!**

```ruby
uangKantin = 500

# Baca: Kecuali Coki punya Uang di atas Seribu, Mending dia Pilih Gausah Jajan!!
# (Karena Uang cman 500... Berarti FALSE (Bohong gada seribu).. MAKA PROGRAM INI YG Malah Di JalANIN!)
unless uangKantin > 1000
    puts "Sabar coki.. lo kaga usah jajan dlu hrini!"
end
```

## 3. Looping Times (Mengulang Kayak Manusia)

Kamu mau nulis kata Halo 5 kali? 

**DI RUBY CUMA KAYA GINI!!**
```ruby
# Panggil angkanya.. Suruh dia ngulang sndiri TIMES ! haha
5.times do
    puts "Halo bos sayang!!" 
end

# Mau ngabarin putarannya udampe mana?? 
3.times do |indeksTugas|
    puts "Lari ngelinging tugu ke- #{indeksTugas}" # Index mulai Dari 0 inget
end
```

Sangat luar biasa kan? Ini alasan developer Startup memuja-muja bahasa Ruby.
---
[⬅️ Sebelumnya](../01-Dasar-Dasar/README.md) | [Lanjut ➡️](../03-Array-dan-Hash/README.md) | [🏠 Daftar Isi](../README.md)
