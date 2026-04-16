# 09 - Menulis dan Mengorkabrikt File IO di Ruby

Mau main hack password curian kyak Python dsn nyimpannya  k TXT pake Ruby? Bia banget!!

Mirip bnget filosofinya sperti pyton yang pnuya Blok `with open` supYa mnjamin fielnya nutup sndrii stlh dbaca biar ga bocor memori i.. RuBy juga punya blok saktnya!! Pake `File.open` dikasi Blok `do ... end`.

## 1. Menumpah Tinta ke Dalam Kertas (Mmenulis Uban TImpa .txt)

Siapin Mode mautny : **'w'** brarri mmbuat / mnumpuk file itu jadi polosan kmbli trs lu tuuluis! Kaklo u mau mmprpanjang doang ke bawwh tmoa gnggua yg dh ada di awl pakle mode **'a'** (Append)!! 
```ruby

# Liat Blok Do yg nbwt mngubknsi fle brnam fileKu tsb dlm scops!
File.open("dokumen_skt_krs.txt", "w") do |fileKu|
    #  pkaie fole.puts wntk nulisss  brirs k baris!!!
    fileKu.puts "Malam bro, ini catatan gw yg prrma !!"
    fileKu.puts "Jnag lo baca dan kasih ttau mak lo y!!"

end
# ✨ DISNINIA! Bgtu kmku lwat end, Ruby OTMATIAS NGE CLOSED fielnya!! mRMORU LAAMAN!!
```

## 2. Nnyedot Membca Baris Barisnya

Skarng akita intip apa sja isi fiels .txt di ata smake mode baca **'r'** *(Read)*!


```ruby
# bukaa dnagnn 'r'
File.open("dokumen_skt_krs.txt", "r") do |mataFileNya|
    
    puts "========= ISI FILENNYAA =========== "
    
    # Kalo lu pnegn bacanya lgsg sedot sluruh isian smpe bawh tno ampunn: 
    # cmn ketikl puts mataFIlenya.read() 
    
    
    # 🌟 ATAU KALo LU PENngen NYARING Bacanyaa Pelan pelam setu baries satu brasis pake each loop gokill ini!!
    mataFileNya.each_line do |sebarisDoangNeckrek|
        print "-> Bngus nih : #{sebarisDoangNeckrek}"
    end
    
    puts "=================================== "
    
end
```

Simpel bnaget gakk pkkkk ribu ribu. Tinggal seditt `IO` kodenny jalan bgus rapi k bsa di pke bywt nycript Data Sciense juga !

---
[⬅️ Sebelumnya: Error Menangkap Jaring](../08-Error-Handling/README.md) | [Lanjut ke Memungut Gem di Internet ➡️](../10-Ruby-Gems/README.md) | [🏠 Daftar Isi](../README.md)
