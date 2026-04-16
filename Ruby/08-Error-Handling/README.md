# 08 - Penjara Kehancuran (*Error Handling*) 

Pasti kesel kalo lo bikin Bot Scraper pengambil harga TIKET Traveloka tiap malam.. Terus jam 3 Pagi web sana mati down.. Si Script Ruby mu ini ikuttan NGE HANG dan KELUAR MERAH FORCE CLOSE dari layar Server VPS!!

Biar Programmu pantang menyerah nge-bypass error, kurung dalem *Begin & Rescue*. (Klo di bahasa lain sebutannnya itu try sm catch).

## Kurungan Tameng `begin` ... `rescue`

Sperti biasaya.. gada kurung kurawal. 

```ruby
puts "--- Sistem Pemantau  Dimuai ---"

begin
    puts "Otw nembak server tiket mereka..."
    
    # NGESENGAJAIN BIKIN ERROR MURNI BIAR MELEDAK! 
    # (Mana bisa membagi angka di dunia ini sama 0)
    uangMngktill = 10 / 0 
    
    puts "Baris ini ga kan kecetak!"

# KURUNGAN PERETAK PENYELAMAT! BEGITU MELEDAK DIA JALAN KESINI:
rescue ZeroDivisionError => bungksCrahnya    
    
    puts "Waduh gile lu bro lu blih mbyagi ngaka nol yak??"
    
rescue StandardError => bungkusUmum
    # Error global lainnya akan jatuh ke jaring ini:
    puts "Ada error laen nhh: #{bungkusUmum.message}"

# PENUTUP RUTINITAs WAJIB APAPUN YANG TERJADI!
ensure
    puts "-- Udh yah, aku selesai dan gak jd nge-Crash! ---"
end
```

Dengan ngerti pola maut begin-rescue... App API Ruby on Rails lo di server Linux bakal tegar bertahan berbulan bulan tanpa takut force closed lg .
---
[⬅️ Sebelumnya](../07-Modul-dan-Mixin/README.md) | [Lanjut ➡️](../09-File-IO/README.md) | [🏠 Daftar Isi](../README.md)
