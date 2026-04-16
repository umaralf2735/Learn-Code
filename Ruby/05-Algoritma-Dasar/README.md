# 05 - Algoritma Dasar Sakti Tembus Batas (*Enumerable*)

Ini alasan Startup Web Amerika thn 2012an nyari Ruby Dev gede gedean gajinya! **ENUMERABLE**.
Lo gak perlu algrotime Looping For-while gkjls untuk misain data, motong text trkecil dll ke k dlam array milih 1-1 kek di bahasa C.

Sama Kerenya sperti Map dan Filter (*JS List Comprehension Python*). Ruy puny Block Yield Maut!!

## 1. Perputaran `.each` (Sang Pengganti LOOP FOR Tuhannn)

Cukup Pake `.each do |variableSmentara|`. Loop C murni lo bakal tamat mati dikubur selamnaya!

```ruby
karyawanPabrik = ["Robby", "Ganteng", "Makmur"]

# Mutar Muterin Semuany: Baca: Setaipp isi karywn pbrik masukin tmpung ke dlam var orang! 
karyawanPabrik.each do |orang|
    puts "Mandor mukulin bngung anak ini: #{orang}"
end
```

## 2. Memetakan Metamorfosis Array Baru `.map`
Sama ke JS persisssssss!!! Ngubah smeua isi data mentah 1-1 dikalilin 2 tanpa numburk ram utamnnya jdilah array anyar!

```ruby
isiDebit = [500, 10, 50, 2]

# Bikin bnsgts lgsung Array bru!! 
# BACA MUDAHNYA DR BWAH INI : Lakukan map dr isidibit sboagi 'ongok' lalu returkan hasil onkkok di kali serbii!!
uangMeledakMega = isiDebit.map do |ongkok|
    ongkok * 1000  # Inget kn gaprulu dksih rturn2 lg auto kpsg diRuby!
end

puts uangMeledakMega.inspect # Print array mode liat siku [] # hsl: 500ribu, 10ribu, 50rbuu
```

## 3. Hakim Pemilah Hukuman Mati `.select`  (Sama kaya JS FILTER)

Misahin misal ada ratusan Object Data Pendudk , lo mau nangkep Org berumu di atas 18 taun buat dpilih jd pmiilu!

```ruby
nomorKeramatSakti = [1, 5, 2, 8, 10, 99, 11]

# Ambil dan tarik ke araray luarr cmn bst angkat GENAP (even?) aja doang cuy!! 
ganjilanDoankNih = nomorKeramatSakti.select do |n|
    n.even?  # ADA FINGSI BAWAANN NAMANy (.even?) tanyak : euy lui genap yakk bos?? (Returtntrue)
end

puts ganjilanDoankNih.inspect # Output -> Haa cuman [2, 8, 10] yg lolos keangkut genap smua!!
```

Ini adalah kempuan pamungkas dari Rails untuk menyaring Ratusan Ribu baris Query Datatbese PstgerSQL mu taroan ActiveRcorsd tnpa PC server lu angsu meledak keabisan Ram mnddak. Semuany krn efesiensinya block Enumerable init ! Mantab !!

---
[⬅️ Sebelumnya: Fungsi Func Def ](../04-Metode-dan-Blok/README.md) | [Lanjut ke Blueprnt Class OOP Ruby Bneran ➡️](../06-OOP-Class/README.md) | [🏠 Daftar Isi](../README.md)
