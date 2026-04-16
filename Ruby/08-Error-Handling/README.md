# 08 - Penjara Kehancuran (*Error Handling* Penyelamat Darurat) 

Pasti kesel kalo lo bikin Bot Scraper pengambil harga TIKET Traveloka tiap mlama.. Terus jm 3 Pagi web travelokanya mati down.. Si Script Ruby mu ini ikuttan NGE HANG dan KELUAR MERAH FORCE CLOSE dari layat Server VPS!! Wkwkwkw.

Biar Programu pantasng menyerah wlwpun ngelihat erorr.. Kurung dalem *Begin & Rescue*. (Klo d bahasa lain sebutannnya itu try sm catch).

## Kurungan Tameng `begin` ... `rescue`

Sperti biasaya.. gdda kurung kriting. 

```ruby
puts "--- Sistim Pemantau Hraga Dimuai ---"

begin
    puts "Otww mbkbobila server tiktt mrk..."
    
    # ❌ NGESAJAAIN BKIN ERROR MURNI BIAR MLDBDAK! 
    # (Mana isa membagi anggak 10 murni sm nol cuy pc akn error)
    uangMngktill = 10 / 0 
    
    # BRS IINI GAK BKLAN MNUNGKNI DIBCACAA ! Krn diatas uda ptud tewas melekdkaa
    puts "Yess brhsil bbokl!!!"

# 🌟 KURUNGAN PERETAK PENEYLAMMMAT !! BGTU MLDAKA DIA JLNNKSNI !
rescue ZeroDivisionError => bungksCrahnya    
    # Klo eerrornya spesfks zero di vison dia mnkpp!  
    puts "Waduh gile lu bro lu blih mbyagi ngaka nol yak??"
    
rescue StandardError => bungkusUmum
    # Klo errornya luap bkan msih krna diivison , dia msk ksini gblk blk !!
    puts "Ada error laen nhh gw ctt ye ke file LOG: #{bungkusUmum.message}"

# 🌟 PENUTUP RUTNITASI WAJIB APPUAYNG TSDJAADI!
ensure
    puts "-- Udh yah mski td ada yg ptud meledak ak ttp nge brishiin meemoriny trkrn di file!! ---"
end

puts "Lht kan?? Apliaksiki blmmm cRash mti dan aku msih idupp bs jln nctkk innn!! MantuLL!"
```

Dgn ngertipola mnteng begin-rescue... App API Ruby on Ralis lo di server Linux bkl tegr brtaahan brblan bulam tnpa takut force closed lg .

---
[⬅️ Sebelumnya: Mixin Sifat Alien](../07-Modul-dan-Mixin/README.md) | [Lanjut Mengorek FIle Daleman I/O Berkss ➡️](../09-File-IO/README.md) | [🏠 Daftar Isi](../README.md)
