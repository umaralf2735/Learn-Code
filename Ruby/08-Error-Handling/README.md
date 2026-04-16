# 08 - Error Handling di Ruby (Begin, Rescue, Ensure)

Ketika program Ruby kamu berinteraksi dengan API atau file luar, besar kemungkinan program akan mendadak tewas ketika barangnya gak ada. Di Ruby, penyelamat nyawa tersebut bernama Exception Handling mengggunakan formasi `begin-rescue`.

## Menangkal Crash Kode

Letakkan semua asumsi berbahaya di dalam `begin`, lalu tangkap bom kesalahannya pada jala penangkap bernama `rescue`.

```ruby
def buka_berkas(nama_file)
  begin
    puts "Mencoba membuka berkas sakral..."
    
    # KODE INI RAWAN AMBYAR KALAU FILENYA GAK ADA YAKAN!!
    isi_file = File.read(nama_file) 
    
    puts "BERHASIL: isinya adalah #{isi_file}"
    
  rescue => e # e adalah variabel penyimpan error yang ditangkap
    puts "WADUH! Gagal men!! Sistem memberitahu:"
    puts ">> #{e.message}"
    
  ensure 
    # Persis seperti finally di bahasa lain
    # Blok ini SELALU terpanggil baik programnya mledug atau normal jaya  
    puts "[Info] Blok pemrosesan berkas 100% selesai."
  end
end


buka_berkas("file_tersembunyi.txt")
```

Kalau kamu ngga pakai begin-rescue, maka saat filenya tak ditemukan programnya bakalan nge-TUTUP seketika! Gak kebayang kan kalo server *Rails* mu mendadak mati sendirian?

---
[⬅️ Sebelumnya: Modul dan Mixin](../07-Modul-dan-Mixin/README.md) | [Lanjut ke Manipulasi Berkas ➡️](../09-File-IO/README.md) | [🏠 Daftar Isi](../README.md)
