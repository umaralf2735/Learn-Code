# 09 - Menulis dan Membaca Berkas (File I/O Ruby)

Mau nyimpen hasil pendaftaran JSON ke .txt pake Ruby? Gampang banget!!

Mirip banget filosofinya seperti python yang punya Blok `with open` supaya menjamin filenya tertutup otomatis memori ngga bocor.. 
Ruby juga punya blok saktnya!! Pake `File.open` dikasi Blok `do ... end`.

## 1. Menumpah Tinta ke Dalam Kertas (Mode Tulis 'w')

```ruby

# Liat Blok Do yg nbata mngunci akses file dlm scopes!
File.open("dokumen_rahasia.txt", "w") do |fileKu|
    
    fileKu.puts "Malam bro, ini catatan gw yg prtama !!"
    fileKu.puts "Jangan dibaca ok!!"

end
# DISINI! Begitu program lewat end, Ruby OTOMATIS NGE CLOSED filenya!! MEMORI AMAN!!
```

## 2. Nyedot Membaca Baris Teks (Mode Baca 'r')

```ruby

File.open("dokumen_rahasia.txt", "r") do |mataFileNya|
    
    puts "========= ISI FILENNYAA =========== "
    
    # Kalo lu pengen bacanya lgsg sedot sluruh isian smpe bawh tno ampunn: 
    # cmn ketik: puts mataFileNya.read() 
    
    
    # ATAU KALo LU PENngen NYARING Bacanya Pelan pelan setu baris satu baris pake each loop!!
    mataFileNya.each_line do |sebarisDoang|
        print "-> Bacaan: #{sebarisDoang}"
    end
    
    puts "=================================== "
    
end
```

Simpel bnaget gakk pke ribet!! Script data science dan web dev butuh ini banget!
---
[⬅️ Sebelumnya](../08-Error-Handling/README.md) | [Lanjut ➡️](../10-Ruby-Gems/README.md) | [🏠 Daftar Isi](../README.md)
