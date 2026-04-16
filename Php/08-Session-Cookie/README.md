# 08 - Menjaga Ingatan Identitas Login (Session Server)

Ada cacat fatal dalam teknologi Website (HTTP Protocol). Website itu punya penyakit Dementia Alzhaimer permanen alias Murni Pelupa (Stateless).

Kalau kamu naruh logic ngecek Login Pake `$_POST` Password di halaman **PROSES**. Dan kamu berhasil Login masuk ke dalem Website. 
BOOM... BEGITU KAMU KLIK MENU "*Ubah Profil*" (Artinya Browser mu memuat File ke -3 (`profil.php`). Si file php ke-3 iku TERNYATA GAK NGENAL KAMU! WKWK! Die nnya "Loh Lu siapa anjir.. Login dlu Sono!" . Koplak kan?! Lah padahal lu udah Login wkwk.

Itulah gunanya Diciptakan **SESSION** *(Menitipkan data ke gembok Memori RAM Server untuk ngantongin Tanda Pengenal khusus Punya Kamu Doang slama browser itu belom nyilang Tabnya)*. 

## 1. Menyiapkan Koper Ingatan

Setiap lembar halaman file PHP yang didalemnya pengen mengecek Login akun tersebut, Tetes pertama airnya di Baris 1 Mentok **HARUS SESAJENKAN MANTRA:** `session_start();`.

**File ke 1: `login_berhasil.php` (Server naruh Gelang Tiket Dufan ke tangan mu)** :
```php
<?php
    // Tancap gass bilang k Mesin Nginx/Apache buat mmbka jatah RAM tuk 1 User ID ini
    session_start(); 
    
    // Anggap lu baru kelar ngetik $Post Password DB dan berhasil Valid...
    
    // Gantungin Tiket Rahasiany!! Simpan datanya di Global Variabel SUPER INI:
    $_SESSION['usernameku'] = "bang_toyib";
    $_SESSION['hakAkses'] = "ADMIN_RAHASIA_NEGARA";
    
    echo "Horee Login Bener dan Sukses Terverifikasi!!";
?>
```

## 2. Membongsai Tiket Di Halaman File Lain (Cek Login Penjagaan Ghaib)

**User Membuka Link LOMPAT FILE ke `dashboard_rahasia.php` :**
```php
<?php
    session_start(); // Mulai lagi biar radar satelit nya Nangkep Gelang diTangan Lu lagi dr Coki nya

    // ISSET adalah fungsi Cek: (Apakah kunci array ini TERISSI BUKAN KOSONG / Udah dibikin)?
    if (isset($_SESSION['usernameku'])) { 
        
        // Wah beneran ada isinya! Die Belom nutup Browser! OKE LAYANI!
        echo "Selamat datang yang mulia Baginda " . $_SESSION['usernameku'] . " Owh.. Anda jabatan: " . $_SESSION['hakAkses'] . "! ";
        
    } else {
        // MAALIN MALING!! BELOM LOGIN MAEN BYPAs NGETIK URL!
        echo "MAAF MINGGGGGGIR, GAK PUNYA TIKET! MUKA LU BELOM DIKENAL! HALAMAN DITOLAK BINGGO!!";
    }
?>
```

## 3. Berpulang dan Membakar Memori Ingatan (Tombol LOGOUT)

Kalo kamu ga neken fungsi Logout, Akun kamu bisa kecolonga bocah lain yg maken PC warnet mu dan langsung ngebuka Seession nya lg!!
Bikin 1 file kusus buat diteken pas misalny di Klik Tombol Logot:
```php
<?php
    session_start(); // Harus mulai dlu radarnya
    
    // INILAH PERONTOK BONGKAHAN CACHE INGATAN SERVER MURNI SEAKAR-AKARNYA! Gelang Gelang di hancukan!
    session_destroy();   
    
    // TRus fungsi header buat nendang nge-Redirect layar dia secara paksa mental pindah ke Halaman Login Awl.
    header("Location: hlaman_login_awal.html"); 
    exit;
?>
```

Ajaib bangett!! Dengan pemahaman Array Session dan Form HTTP dari Bab sebla, kamu skrng sdh tau tulang punggung dan otot geraj utama Pemrograman Web Fullstack dinamis!! Tinggal 1 langkah lagi: (DATABASE).

---
[⬅️ Sebelumnya: HTML Post Form](../07-Form-Method/README.md) | [Lanjut ke Membobol Database ➡️](../09-Koneksi-Database/README.md) | [🏠 Daftar Isi](../README.md)
