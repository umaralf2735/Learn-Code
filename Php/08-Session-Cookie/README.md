# 08 - Menjaga Ingatan Identitas (Session Server)

Website itu sifatnya pelupa gais. (Amnesia/Stateless).
Jadi kalau kamu Login di halaman A. Waktu kamu masuk ke Link ke halaman B, dia udah gak ngenalin kamu lagi, lu disuruh login ulang. Konyol kan?

Itulah kenapa diciptakan **SESSION** (Penyimpanan nyawa sementara di RAM Server khusus orang tsb).

## Menyiapkan Koper Ingatan

Setiap halaman PHP yang pengen ada sistem "Ingatan Akun / Keranjang Belanja". Baris paling atas dari atasnya PHP *HARUS ADA MANTRA* `session_start();`.

**File `login_berhasil.php` :**
```php
<?php
    session_start(); // Tancap gass buka RAM Server untuk user ini
    
    // Anggap lu baru kelar cek password di Database
    // Simpan kunci rahasianya buat dia keliling halaman!! (Kek gelang tiket wahana Dufan)
    $_SESSION['username'] = "udinsuper";
    $_SESSION['peran'] = "ADMIN_RAHASIA";
    
    echo "Login Sukses!!";
?>
```

**LALU USER BUKA HALAMAN DASHBOARD RAHASIA (`dashboard.php`) :**
```php
<?php
    session_start(); // Mulai lagi biar gelangnya ke tracking lagi

    if (isset($_SESSION['username'])) { 
        // Apakah gelangnya valid nempel?
        echo "Wah.. admin agung " . $_SESSION['username'] . " Tiba! Menundukk!!";
    } else {
        echo "MAAF LU SIAPA? HALAMAN DITOLAK!! BELOM LOGIN LU!";
    }
?>
```

**Bagaimana Menghancurkan Identitasnya (Bila Pencet Tombol Logout?)**
Tinggal panggil di file baru:
```php
<?php
    session_start();
    session_destroy();   // Membakar ingatan user ini dari server!
    header("Location: index.html"); // Nendang dia balik ke luar
?>
```

Sip, kalian sudah sah menguasai sistem pintu akses Keamanan Website tingkat pertama!

---
[⬅️ Sebelumnya: Form Get Post](../07-Form-Method/README.md) | [Lanjut ke Menyadap Database ➡️](../09-Koneksi-Database/README.md) | [🏠 Daftar Isi](../README.md)
