# 07 - Class OOP Strict (Private / Public)

Sama kek ES6 Class Javascript modern, TAPI sekarang TS memasukkan unsur Mutlak dari Java C#, yaitu Security Key: `private`, `protected`, dan `public`!!

## Membungkam Variabel Rahasia

```typescript
class RekeningBank {
    public namaPemilik: string; // Bisa diintip dicode luar pake .namaPemilik
    private saldoRahasia: number; // 🔒 DIKUNCI RAPAT GABISA DILIHAT DARI LUAR CLASS!!

    constructor(namaPemilik: string, saldoAwal: number) {
        this.namaPemilik = namaPemilik;
        this.saldoRahasia = saldoAwal;
    }

    // Tapi didalam Class yang sama, fungsi ini bisa mengakses Private tsb
    public getSaldo() {
        return `Ssstt... Uangmu sisa Rp.${this.saldoRahasia}`;
    }
}

const rekAndi = new RekeningBank("Andi Setiawan", 500000000);

console.log(rekAndi.namaPemilik); // ✔️ BISA DIBACA
// console.log(rekAndi.saldoRahasia);  // ❌ MERAH ERROR!! VARIABLE PRIVATE TERTUTUP!

console.log(rekAndi.getSaldo()); // ✔️ JALAN BELAKANG AMAN!
```

Disinilah Typescript beneran membuat Javascript layak dipakai di sistem Perbankan / Backend Nest.JS Super Secure!

---
[⬅️ Sebelumnya: Interface](../06-Interface-dan-Type/README.md) | [Lanjut ke Enum ➡️](../08-Enum/README.md) | [🏠 Daftar Isi](../README.md)
