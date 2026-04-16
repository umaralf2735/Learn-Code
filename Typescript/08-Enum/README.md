# 08 - Enum (Pecahan Status Rapi)

Kalau kita sering bikin kondisi misal: Web sedang Muter, Web Error, atau Web Selesai narik. Kita kan kadang nulis String manual: `"Lagi Loading"` atau `"Udah Sukses"`. Gawat klo TYPO.
Enums hadir menyelamatkan dari Typo Status.

## Mengikat Status Permanen

```typescript
// Ibaratnya Dictionary yang sudah baku valuenya.
enum StatusTransaksi {
    MENUNGGU_BAYAR = "MENUNGGU_BAYAR",
    SEDANG_DIKIRIM = "SEDANG_DIKIRIM",
    SELESAI = "SELESAI",
    GAAGAL = "GAGAL"
}

// Bikin fungsi yg menuntut status asli ENUM diatas
const ubahResi = (tandaPengenal: StatusTransaksi) => {
    if (tandaPengenal === StatusTransaksi.SEDANG_DIKIRIM) {
        console.log("Mantap paket jalan di tol!");
    }
}

// MANGGILNYA GAK NGETIK TEKS BISA TYPO. MANGGILNYA PAKE DOT OBJECT!
ubahResi(StatusTransaksi.SEDANG_DIKIRIM);
```

Penggunaan Enum meminimalisir Database nyimpen Typo teks dari Aplikasi mu di Production!!

---
[⬅️ Sebelumnya: OOP Class](../07-Class-OOP-Strict/README.md) | [Lanjut ke Generics Lanjut ➡️](../09-Generics/README.md) | [🏠 Daftar Isi](../README.md)
