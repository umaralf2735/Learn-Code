# 10 - Membendung Sistem dengan Virtual Environment (VENV)

Bab ini adalah senjata peradaban paling krusial ketika kalian terjun menjadi Developer Python asli/asli merintis startup.

## Masalah Kehidupan

Di Javascript (`NPM`), setiap komputermu download library maka folder terletaknya secara default itu menumpuk di `node_modules` **di dalam** folder projek kamu.

Sayangnya Python tua itu kelakuannya lain! Semua `pip install` itu dimasukkan menumpuk dan mendeselin `OS Komputer Terdalammu` (Local Program Files Install). Alhasil kalau Projek A butuh `Versi 1`, dan projek B butuh `Versi 3`. Nanti waktu di run bentrok semua error!!

## Solusi Dewa: Pembatas Siluman (`VENV`)

Daripada merusak sistem asli, kita sihir terminalnya bikin kloningan kotak pasir python kecil dilokasi khusus Project situ aja!

**1. Membuat Wadah (Bikin hanya 1x di awal Project)**
Di terminal foldermu ketik perintah (ini bawaan dari pythhonnya):
```bash
python -m venv kandang_siluman
```
(Akan tercipta folder benama 'kandang_siluman' beneran didalammu!)

**2. Memasuki Alam Bawah Sadarnya (Activate)**
Kalian WAJIB ngeklik portal ini sebelum mulai ngerjain projek apapun di sana!
Kalau di Windows PowerShell:
```powershell
.\kandang_siluman\Scripts\Activate.ps1
```
*(Kalau di Mac/Linux pakai: `source kandang_siluman/bin/activate`!)*

**3. Bukti Tersihir**
Nanti kalau terbukti berhasil, tulisan Shell kalian di sebelah kiri mentok akan berubah nama bertambah menjadi `(kandang_siluman) D:\Folder_kerjamu...` 

Nah kalau itu udah ada, seluruh `pip install` tak pernah menyentuh file instalasi Windowsmu lagi dan aman diisolasi!  Cara cabutnya tinggal run `deactivate`. Superrrr kan!

---
[⬅️ Sebelumnya: File IO](../09-File-IO/README.md) | [🏠 Daftar Isi Utama](../README.md)
