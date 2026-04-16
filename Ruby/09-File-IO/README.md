# 09 - Menulis dan Membaca Berkas (File I/O)

Sebagai bahasa script pelampiasan bahagia, mengubah nama ratusan file teks pakai satu kali enter di Ruby itu enteng sekali. Class bernama `File` bisa mengabulkan itu tanpa *download library* sana-sini!

## 1. Membaca Berkas (.txt, dll)

```ruby
# Anggap kamu punya catatan.txt

# --- CARA PERTAMA (Bikin pegal kudu buka tutup memori manual) ---
fileku = File.open("catatan.txt", "r") # "r" itu mode Read
puts fileku.read
fileku.close # AWAS JANGAN LUPA NUTUP KERAN NYA

# --- CARA KEDUA (Ruby Ways!) Otomatis tutup memori tanpa repot ---
isi_konten = File.read("catatan.txt")
puts isi_konten
```

## 2. Menulis / Membuat File Baru

Disini mode huruf akan menentukan:
- `"w"` (Write): **MENIMPA** penuh semua file isi catatan kalau memang sudah ada filenya.
- `"a"` (Append): **MENAMBAHKAN** sisipan tulisan ke bawah teks lama!

```ruby
# KITA BUAT FILE TULISAN BARU:
File.open("hasil.txt", "w") do |dokumen|
  dokumen.puts "=== DATA BARU BIKINAN RUBY ==="
  dokumen.puts "Program ini telah dieksekusi secara ghaib hari ini"
end

puts "Berkas Hasil sudah ditelurkan di foldermu!"

# KITA COBA NAMBAHIN DARI BAWAH:
File.open("hasil.txt", "a") do |dok|
  dok.puts "Oh iya aku lupa nambahin ini.."
end
```

Sekarang kamu sudah jadi *hacker* pengubah teks sejati di PC mu!

---
[⬅️ Sebelumnya: Error Handling](../08-Error-Handling/README.md) | [Lanjut ke Ruby Gems ➡️](../10-Ruby-Gems/README.md) | [🏠 Daftar Isi](../README.md)
