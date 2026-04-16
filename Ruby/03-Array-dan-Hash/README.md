# 03 - Penyimpanan Sekardus (Array & Hash Symbols)

Gak nendang kita gabisa manipullasi Banyakn data orgn seklaigus kalau ga ada Array. Ruby memilikinya. Tapi fitur maut ada pada Dictionary / Object Json nya Ruby yg dinamakan sbg `Hash`!

## 1. Array Dinamis Melar

Kaya Python. Array nya Ruby ga usah dipesen brap ukuran dan tipe datanya. Melar molor nabrak campur baur sah aja.

```ruby
# Tuh wkwk angka nyatu campur ma Text maut
lokerBarang = ["Pistol Kayu", "Garam", 99, false]

# Nambah pki PUSH biasa (Ujunng kanan)
lokerBarang.push("Botol Air")

# MENGAKSES NYA?
puts "Senjata petama saya adlah: #{lokerBarang[0]}"

# 🌟 ALAT PISAU DEWA RUBY! Punya alat ngmbil prtama dan trpntar tnpa nyar idnex!!
puts "Ujung DEPAN : #{lokerBarang.first}"
puts "Ujung BLAKNG: #{lokerBarang.last}"
```

## 2. Hash & Symbols (Sang Object Penakluk Data JSON)

Di PHP in dinamin Array Assossiatif. Di Python ini itu sebutnnya Dictionry. Inilah Hash. Punya Kunci Teks (Key : Value) berpasangan dlmKurawal `{}`.

Di Ruby, untuk mengirit RAM Supaya **Kuncinya GAK DICOPY BERKALIKALI JADI STRING RAM MURNI**, mrk nyiptain yang namanya `SIMBOL (Tanda Titik dua diDEPAN TEKS `:kuncigue`)!!` Ini lbih enteng drpd string "kuncigue" biasa!

```ruby
# Nyetak Objk json Hash milih Coki
bukuRekamMedis = {
    :namaPasien => "Bang Toyib",
    :riwytSakit => "Masuk Angin Tolak",
    :umur       => 45
}

# NGAMBILNYA? LU HARUS PANGGIL 'ALAT TUKAR' SIMBOLNYA YA!! (Bkn ktip String!!)
puts "Dokter tlong prksa bapak #{bukuRekamMedis[:namaPasien]}"

# Nambah Data Gejala Bru
bukuRekamMedis[:suhuBadan] = 39.5
```

**💎 TRICK PENULISAN DEWA JS STYLE:**
Kalau capek nulis Panah `=>` gemuk gitu kek PHP. Kalian BOLEH nulis gayak Javascript. Tarik titik duanya ksamping! Ruby bakal sngja ngebikin dkk jadi Symboll ghaib d blkng layar.

```ruby
# INI SAMA AJA KAYA DIATAS!! LBH RINGKAS KAN KEK JAVASCRIPT! LBH CKEP!
bukuBaru = {
    namaPasien: "Ridho Ilahi",
    umur: 20
}

puts "Siank bang #{bukuBaru[:namaPasien]}" # MANGGIL BWHNYA TTEP WAJIB PAAKKE TTTiK dua SIMBOL DEPAN Y!
```

Nanti kalau kalian pake Ruby on Rails sbg API server, smua JSON request yg dilempar Frontend React bkl dsulap murni jd hASH Ruby kya dpan mtamu ini!!

---
[⬅️ Sebelumnya: Sruktur Kondisi IF](../02-Struktur-Kontrol/README.md) | [Lanjut ke Fungsi Sakti (Def) ➡️](../04-Metode-dan-Blok/README.md) | [🏠 Daftar Isi](../README.md)
