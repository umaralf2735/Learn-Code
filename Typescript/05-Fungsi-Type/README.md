# 05 - Fungsi Berkelas (Return Value Strict)

Semakin membabi-buta sebuah fungsi di JS, kalian tak bisa melacak apa yang di-Return. Entah yang *dipulangin* itu Data atau Error Text. Disini kita ikat hasil keluarannya!

## 1. Menjanjikan Hasil Return Mutlak

Berikan Type setelah kurung parameter `): tipe {` !
Maka dengan ini Fungsi JS mu auto menjadi sakti laiknya Golang.

```typescript
// Fungsi ini DIWAJIBKAN mereturn Number gak boleh text!
const kalkulasiKeuntungan = (modal: number, jual: number) : number => {
    let untung = jual - modal;
    
    // Kalau dibaris ini gue return "Lima Puluh"; TS Bakal Error Merah!
    return untung; 
}

console.log( kalkulasiKeuntungan(50, 100) ); // 50
```

## 2. Type Void Hampa

Sama ibarat bahasa C dan Java. Kalau lu cuman nge-print *console.log* dan ga pake statement `return` di dalemnya... tandain tuh Fungsi pakai `: void` !

```typescript
const siramTanaman = (namaGeng: string): void => {
    console.log(`Menyiram geng nya ${namaGeng} siang ini bosku..💦`);
    
    // Disini lu dilarang keras return "Selesai" , harus dibiarin Hampa!
}
```

Disadari tidak sadar, semakin TS ditegakkan, semakin JS mu rasanya "Bau OOP Kental" kaya Java haha. Emang tujuannya ngerubah orang FrontEnd liar menjadi *Software Engineer* terstruktur!

---
[⬅️ Sebelumnya: Array dan Tuple](../04-Array-Serta-Tuple/README.md) | [Lanjut ke Tahap Lanjut (Interface) ➡️](../06-Interface-dan-Type/README.md) | [🏠 Daftar Isi](../README.md)
