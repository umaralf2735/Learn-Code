# 02 - Struktur Kontrol (If, Else, dan Magis `unless`)

Mari kita bahas IF ELSE nya. Ingt yg diawal kubilang, ngga ada Kurung Kurawal `{ }` pusing lagi. 
Sebagai gantinya. Kalian diwajibkan Mengunci gerbang Logikanya Pukul Rata Pakai Tulisan **`end`** dibawahnnya!!

## 1. Percabangan dengan `if` dan `elsif`

Perhatikan! bukan Else If yak, TAPI disingkat mnjd **`elsif`**!!

```ruby
darahMusuh = 25

if darahMusuh >= 50
    puts "Maju teruss tank nya tbbel bosque!"
    # LU BEBAS ngetik sepanjang aappapun ksini turun kdwbah trsu gapapa .

elsif darahMusuh >= 15
    puts "Sikat udah Sekarat nanggung!"
else 
    puts "Hit sekliklagi mati!!!"
end # INI WAJIB! SBGAI PENGGANTI KURUNG PENUTUP } MURNI!!
```

## 2. Sang Pelawan Arus Sakti (`unless`) 

Kalo di bahasa C lu nulis syarat tidak sama dengan kayak gni "Kalo GAK Ujan" : `if ( !hujanAman )`. Ngetik TANDA SERU `(!)` kadang suka sliut nyempil g gampang diliat mata org.

Ruby nyiptain kata *"KECUALI KALAU..."* (`unless`). 
**Dia bakal Njalanin bloknya KETIKA SYARATNYA BOHONG/FALSE!!!**

```ruby
uangKantin = 500

# Baca: Kecuali Coki punya Uang di atas Seribu, Mending dia Plih Gausah Jajan!!
# (Karena Uang cman 500... Berarti FALSE (Bohong gda sribu).. MAKA PROGRAM INI YG MAALh Di JalANIN!)
unless uangKantin > 1000
    puts "Sabar coki.. lo kaga usah jajan dlu hrini!"
end
```

## 3. Looping Times (Mengulang Kayak Manusia)

Kamu mau nulis kata Halo 5 kali? 
Kalo di C `for(int i=0... dsb.`. Di JS `for(let i=0....)`

**DI RUBY CUMA KAYA GINI!!**
```ruby
# Panggil agnkannya.. Suruh dia ngulang sndiri TIMES ! haha
5.times do
    puts "Halo bos syang!!" 
end

# Mau ngabari putarannya udayampe mna?? 
3.times do |indeksTugas|
    puts "Lari ngelinging tugu ke- #{indeksTugas}" # Index mlai Dr 0 ingt
end
```

Wow wow!! Mulai kelihatan kan seberapa "Human-Friendly" bgt si Ruby inj? Pantek aja Framework RAILS itu dipuji puji kecepatan *Devolopment* dan Codingnya di Amerika thn 2010n !! 

---
[⬅️ Sebelumnya: Dasar Print Output](../01-Dasar-Dasar/README.md) | [Lanjut ke Harta Karun Hash ➡️](../03-Array-dan-Hash/README.md) | [🏠 Daftar Isi](../README.md)
