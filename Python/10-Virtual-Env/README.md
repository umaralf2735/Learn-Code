# 10 - Membendung Sistem dengan Virtual Environment (VENV)

Bab ini adalah senjata dan pagar pembatas peradaban **PALING KRUSIAL** ketika kalian terjun mencari lowongan kerja / gabung Tim Tim Startup memakai Python. Jangan lewati!

## Masalah Kehidupan Orang Miskin (Polusi PIP)

Di Javascript (`NPM`), setiap komputermu download library maka folder terletaknya secara default itu AMAN DITUMPUK LOKAL di `node_modules` **di dalam** Punya Kamu itu aja.

Sayangnya, kalau di Python... Semua `pip install namapackagenya` itu **DI TENDANG CAMPUR ADUK MASSAL MENUMPUK DI ROOT OS KOMPUTER TERDALAMMU (Local Global App Data Window)**. 

Alhasil kalau *Projek Website AI lu* butuh Tensor versi Lawas, dan bsok nya kamu bljar bkin projek robot baru yang kebetulan butuh  Tensor *Versi 3*. BEGITU di install.. dua due versinya BENTROK GIGIT GIGITAN ERROR PARAH karena dicmpur numpuk d system c!!

## Solusi Dewa: Pembatas Siluman (`VENV`)

Daripada merusak sistem asli global komputer, kita ciptakan ruang Ilusi *(Sandbox Virtual Environment)*! Yg mengkurung semua isntalan library PIP itu ga keluar batas kmar folder Project lu itu. 

### 1. Membuat Wadah Kosong (Bikin cuma 1x wkt di awal Project Baru)
Buka terminal cmd mu pada directory projek (misaln `d:/projectGue`).
```bash
python -m venv my_ruang_batas
```
(Tunggu sbntar.. Tiba tiba tercipta lah selipan folder baru `my_ruang_batas` didalem situ yg beratnya lmyan lahh isiny pyton clone!)

### 2. Memasuki Alam Bawah Sadarnya (Activate/Aktivasi)
Ini Hukum Wajib: Kalian SETIAP HARI MAU BUKA KODINGAN HARUS NGEKLIK PORTAL INI sebelum nge-pip apapa!

Kalau di **CMD Windows**:
```cmd
my_ruang_batas\Scripts\activate.bat
```
Kalau di PC **Mac/Linux Terminal**: `source my_ruang_batas/bin/activate`

### 3. Bukti Tersihir Di Alam Siluman
Kalau sudah run berhasil... perhatikan kursor ngedip cmd terminal mu yang disebelah mentok kiri ngetik berubah drsastis ditandain cap nama mapny:
` (my_ruang_batas) PS D:\WebProjekGue> `

NAHHHH KALU TULISAN KURUNG IJO ITU UDAH NONGOL!! Lo bebas berbuat brutal dan jahat *pip install bla*, *uninstall lsa*, Ga bakalan ngerusak Laptop aslinya di belakang!! Semua dipungut kedalem folder venv rapiih !!  Kalo kluar mau cabut ke bumi nyata, ketik aja `deactivate`.  Mantap jiwa!!

----
## PENUTUP PERJALANAN ULAR

Selamat! Kalian telah menamatkan seluruh seluk beluk Bahasa Inti yang paling revolusioner era milenium ini! 
Dengan ini, masukilah dunia Backend Django, FastAPI untuk web. 
Masukilah Dunia Jupyter, ScikitLearn, PyTorch untuk menjadi Dewa AI ! 
Bahasanya tidak akan pernah beda diluar dr 10 Modul Pembahasan yang saya buatkan ini.

---
[⬅️ Sebelumnya: Modifikasi File i/o IO](../09-File-IO/README.md) | [🏠 Daftar Isi Induk Utama](../README.md)
