# 01 - Dasar-Dasar Ruby (Bahasanya Manusia Terindah)

Kenapa kalian harus nyeduh kopi sambil ngoding Ruby?
Karena Ruby diciptakan oleh Mas Yukihiro Matsumoto (Matz) dari Jepang dengan 1 misi gila: **"Membahagiakan sang Programmer, bukan Memanjakan Mesin PC"**.

Bahasanya SANGAT mirip puisi bahasa inggirs biasa. Ga ada kurung kriting nyebelin `{}`, ga ush mencet titik koma `;` . Semuanya ngalir asik. Ini adalah otak dari Startup gila milyaran dollar ky Airbnb sm Twiiter di awl-awal ny gan!

## 1. Nge-Print Suara (Puts)

Ubah kata `console.log` lu yg kepanjangan jadi 4 Huruf doang : **`puts`** 

```ruby
# Lihat? Kaga pake titik koma babar blass!
puts "Halo dunia nyata. Ini gw Ruby programmer baru!!"

# Puts ngasih ENTER garis kebawah otamtis.. Klo lu pengen Nyamping trus ngetiknya PAKE PRINT!
print "Aku nyambung cuy "
print "sok coba lihat no enter kan?"
```

## 2. Everything is an Object! (Murni Benda)

Di Javascript, angka `5` itu kasta rendahan (Primitf) gabisa dikulik propertiesnya. DI RUBY, ANGKA 5 ADALAH SEBUAH BENDA CLASS DEWA CLASSIC YANG PUNYA AKSI NYA SENDIRI!!!

```ruby
angkaDuit = -5000

# Lu bisa lgsun nempelin TITIK ke dikanan Angka itu untuk melakuin Method Class ABSOLUTE murni!!
puts angkaDuit.abs    # Ngerubah Jd Positif = 5000 
puts "Apel".length()    # Ngitung panjang hrud
puts "halo bangsat".upcase   # JADI HURUF GEDEE HALO BGSST!
```

## 3. String Interpolation (Menempelkan Peta Dalam Tulisan) `#{ }`

Daripada capek nutup kutip nyambung kutip trus gado gadoin Spasi pke Tanda + Pluss (+). Ruby punya Pagar Kurung `#{  }` . 
*(Mirip bgt kek Backticknya JS sm f-Stringy Python)*.

```ruby
pekerjaan_gue = "Nelayan Mancing"
gajiPerHari = 50

# WAJIB PAKE KUTIP GANDA LHO YAA BIAR KETEMBUS! (Klo pke kutip satu ' ' si Pagar nya bkal jd print msnta murni tdk menydot data).
puts "Wih gila pak kades gajinya si tukang #{pekerjaan_gue} ternyata sgdek $#{gajiPerHari} dollar!!"
```

Sederhana dan luar biasas menenngkann kalbbu kan ngoding Ruby?. Kodinganmu akan sangat bersih dari polusi simbolik mtmattika Mesin. Lanjut ke alur percabsnagnya yuk!

---
[Lanjut ke Struktur Kontrol Unless ➡️](../02-Struktur-Kontrol/README.md) | [🏠 Daftar Isi](../README.md)
