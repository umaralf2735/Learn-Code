# 10 - Utility Types (Mutator Sakti)

Sebuah interface yang udah terlanjur ditetapin kadang mau kita "Sunat/Potong sebagian" untuk kasus Form Pendaftaran doang (Contoh Database itu Interfacenya nyimpen `id` otomatis dsn `ter-Update-pada`, padahal kalau User Form Daftar baru dia mana tau id nya?!.

## Partial (Bikin semua atribut jadi Optional Boleh Kosong)

```typescript
interface AkunPengguna {
    nama: string;
    noHP: string;
    saldo: number;
}

// BIKIN FITUR EDIT (Kadang yang dikirim cuma nama doang kan ke server, ga semua 3 3 nya penuh?)
// DARIPADA BIKIN INTERFACE BARU "EditAkun". Mending sunat / tempel sihir Partial<> !
function updateAkun(dataSisa: Partial<AkunPengguna>) {
     // Semua di dalem situ otomatis berubah dikasih '?' tanpa nyentuh codingan aslinya
     console.log("Data diproses!");
}

updateAkun({ saldo: 500 }); // AMAN TEMBUS, ga ditagih minta nama!!
```

## Omit (Ngebuang yang Bikin Repot)

"Tolong buatin tipe data Akun, TAPI KECUALI SALDO nya ya bos, ini form ga nanya saldo!"

```typescript
// Membuang atribut tertentu pakai Omit<BlueprintAsli, "YangDibuang">
type AkunTanpaDuit = Omit<AkunPengguna, "saldo">;

const siBoke: AkunTanpaDuit = {
    nama: "Ujang",
    noHP: "0000"
    // GAK AKAN DITAGIH SALDO DISINI! PERFECT!!!
}
```

SELAMAT!! Kamu sah menjadi Mastah Senior Frontend kalau sudah menyerap kekuatan ke-10 Bab Typescript yang paling sering ditanya HRD kalau mau masuk Google/FB/Gojek ! 

---
[⬅️ Sebelumnya: Generics](../09-Generics/README.md) | [🏠 Daftar Isi Utama](../README.md)
