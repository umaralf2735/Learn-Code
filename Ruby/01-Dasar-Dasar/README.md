# 01 - Dasar-Dasar Ruby (Bahasanya Manusia Terindah)

Kenapa kalian harus nyeduh kopi sambil ngoding Ruby?
Karena Ruby diciptakan oleh Mas Yukihiro Matsumoto (Matz) dari Jepang dengan 1 misi gila: **"Membahagiakan sang Programmer, bukan Memanjakan Mesin PC"**.

Bahasanya SANGAT mirip puisi bahasa inggris biasa. Ga ada kurung kriting nyebelin `{}`, ga usah mencet titik koma `;` . Semuanya mengalir asik. 

## 1. Nge-Print Suara (Puts)

Ubah kata `console.log` lu yg kepanjangan jadi 4 Huruf doang : **`puts`** 

```ruby
# Lihat? Gaga pake titik koma babar blas!
puts "Halo dunia nyata. Ini gw Ruby programmer baru!!"

# Puts ngasih ENTER garis kebawah otomatis.. Klo lu pengen nyamping terus ngetiknya PAKE PRINT!
print "Aku nyambung cuy "
print "sok coba lihat no enter kan?"
```

## 2. Everything is an Object! (Murni Benda)

Di Javascript, angka `5` itu kasta rendahan (Primitif) gabisa dikulik propertiesnya. DI RUBY, ANGKA 5 ADALAH SEBUAH BENDA CLASS DEWA CLASSIC YANG PUNYA AKSI NYA SENDIRI!!!

```ruby
angkaDuit = -5000

# Lu bisa lgsung nempelin TITIK ke dikanan Angka itu untuk melakuin Method Class Murni!!
puts angkaDuit.abs()       # Ngerubah Jd Positif = 5000 
puts "Apel".length()       # Ngitung panjang huruf
puts "halo badut".upcase() # JADI HURUF GEDE: HALO BADUT!
```

## 3. String Interpolation (Menempelkan Peta Dalam Tulisan) `#{ }`

Daripada capek nutup kutip nyambung kutip trus gado gadoin Spasi pake Tanda Pluss (+). Ruby punya Pagar Kurung `#{  }` . 
*(Mirip banget kek Backticknya JS lho)*.

```ruby
pekerjaanGue = "Nelayan"
gajiPerHari = 50

# WAJIB PAKE KUTIP GANDA LHO YAA BIAR KETEMBUS!
puts "Wih gila pak kades gajinya si tukang #{pekerjaanGue} ternyata segede $#{gajiPerHari} dollar!!"
```
---
[Lanjut ke Struktur Kontrol Unless ➡️](../02-Struktur-Kontrol/README.md) | [🏠 Daftar Isi](../README.md)
