# 07 - Class OOP Super Strict (Kempesin JS Yang Lemah)

JS modern punya Class. Tapi boong boongan doank. Di JS, semua Variabel/Porperti dalam Class itu Otomatis bisa diintip dan ditusuk orang luar dari luar gembok (Public Murni).

TS datang memmbawa aliran Java: Memperkenalkan `public`, `private`, `protected`.

## 1. Menyegel Pintu Brankas Class

```typescript
class PahlawanSuper {
    // 1. PUBLIC = Siapapun dri file mana aja boleh nrk ngedit isiny (Secara Default sbnernya JS bgini)
    public namaAktor: string;
    
    // 2. PRIVATE = HANYA BOLEH DI UBAH/DIBACA DARI DALEM PERUT FUNGUNGS CLASS INI SENDIRI! Diluar dsana gabsa ngntip.
    private tabunganUang: number;
    
    // 3. PROTECTED = Mirpi privat. Tp ngbolehin anak asuhnya (Yg di Extends/Warisan ) bsa ikut nmkmati ngerbahnya!!
    protected skillSakti: string;

    constructor(nama: string, uang: number, skill: string) {
        this.namaAktor = nama;
        this.tabunganUang = uang;
        this.skillSakti = skill;
    }

    // Karena gw di dalem pnhg class ini, gw bsa numbuk dan bca kktin si private !!
    public intipIsiDompetGueBrapaCuy(): void {
        console.log(`Gua sisa duat Rp. ${this.tabunganUang} aja.`);
    }
}


// --- PENGUJIANNYA DI LUAR ARENA ---

let theFlash = new PahlawanSuper("Barry Allens", 50000, "Lari Cpat Kilat");

// Murni bisa ngganti namnya Krn PUBLUBC !
theFlash.namaAktor = "Bang Flash"; 

// ❌ TS LANGSUNG TERRAK NGAMUK : ERROR KILAT! : Private Property "tabnngan Uang" gbisa diakses darilaUr bungkus!!"
// theFlash.tabunganUang = 99999999; 

theFlash.intipIsiDompetGueBrapaCuy() // Ini bisa mnjalan krena fungsi intpNy bbrbentuk PUBLIC ! Mantaanf!
```

Liat kan skrg kenapa anak Backend Java sering mutasi belot ke *NestJS/TypeScript* bwat msukkin lamaran krja Nodejs? Karma bener bener sama PLEK! Gada rsa ngoding kek org blingsatan ngelag. Semuaya ke segel strict Object Oriented di TS!

---
[⬅️ Sebelumnya: Inaterface Tye Alias](../06-Interface-dan-Type/README.md) | [Lanjut ke Enum Si Pemegang Pilihan Mutlak ➡️](../08-Enum/README.md) | [🏠 Daftar Isi](../README.md)
