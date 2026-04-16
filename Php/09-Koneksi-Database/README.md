# 09 - Menarik Darah Database MySQL (Ilmu Hitam PDO)

Gak seru kalau nyimpan data pakai ngetik list manual. Kita butuh Server DB SQL. PHP memiliki jembatan modern yang tak terbataskan: PDO (*PHP Data Objects*). PDO ini kebal terhadap virus serangan siber *SQL-Injection*. Dahsyat.

## Membuka Sambungan Ke Mesin MySQL Lokal (XAMPP Biasnaya)

```php
<?php
$host = "127.0.0.1";
$db   = "tokoku"; // Anggap nama basis datanya Tokoku
$user = "root"; // Default XAMPP/WAMP
$pass = "";     // Kosong bjasanya

try {
    // Menyusun jimat mantra PDO nya
    $pdo = new PDO("mysql:host=$host;dbname=$db", $user, $pass);
    
    // Menjalankan Tarikan Data
    $pertanyaan = "SELECT * FROM produk LIMIT 5";
    $stm = $pdo->query($pertanyaan);
    
    // Ngenyedot hasil ke Array Assosiatif!!
    $semuaBarang = $stm->fetchAll(PDO::FETCH_ASSOC);
    
    // Buka datanya ke html
    foreach($semuaBarang as $b) {
        echo "Beli Kakaaa: " . $b['nama_barang'] . " Harga: Rp" . $b['harga'] . "<br>";
    }

} catch (PDOException $e) {
     echo "Kiamat Database: " . $e->getMessage();
}
?>
```

Itu dia intisarinya! Kalau mau nyimpen `INSERT` yang aman tanpa di hack orang pakai Bind Param, namun di modul awalan ini, kalian membuktikan bahwa Website dan Database bisa digabung sedemikian apik dengan PHP.

---
[⬅️ Sebelumnya: Session State](../08-Session-Cookie/README.md) | [Lanjut ke Composer NPM ➡️](../10-Composer/README.md) | [🏠 Daftar Isi](../README.md)
