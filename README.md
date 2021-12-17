1.Buatlah skema untuk kebutuhan data profile pengguna aplikasi Skiljek dan relasi apakah yang tepat untuk data tersebut? Data yang dibutuhkan adalah:
Full Name
Email
Phone Number
Jawab : Relasi One-to-one.

**Skema**:
```json
{
  "_id":"ObjectId(61bc99c20ba2597e66a34218)",
  "fullName":"Salsa Hany",
  "email":"salsahany0@gmail.com",
  "phoneNumber":"082269335741"
}
```

2. Buatlah skema untuk kebutuhan data alamat pengguna SkilShop dimana alamat yang dapat didaftarkan maksimal 2 alamat. Jelaskan juga relasi apakah yang tepat untuk data tersebut? Data yang dibutuhkan adalah:
Full Name
Phone Number
Address (Max 2)
Jawab : Relasi yang tepat adalah One To Many
**Skema**:
```json
{
    "_id": "ObjectId(61bc99c20ba2597e66a34219)",
    "fullName": "Salsa Hany Saputri",
    "phoneNumber": "082263790256378",
    "address": ["Aceh", "Langsa"]
}
```

3. Buatlah skema untuk kebutuhan data dari suatu Products yang akan mempunyai banyak varian dari aplikasi SkilShop. Jelasskan juga relasi apakah yang tepat untuk data tersebut? Contoh data yang dibutuhkan adalah:
Product
Product Name: Kaos Polos
Brand Name: SkilShirt
Varian Pertama
Varian Name 1: Kaos Polos Hitam
Color: Hitam
Quantity: 12
Price: Rp 99.000
Varian Kedua
Varian Name 1: Kaos Polos Navy
Color: Navy
Quantity: 10
Price: Rp 99.000
Jawab : Relasi yang tepat adalah one to many
**Skema**:
```json
{
    "_id": "ObjectId(61bc99c20ba2597e66a34220)",
    "productName": "Kaos Polos",
    "brandName": "SkilShirt",
    "variants": ["ObjectId('61bda13798857b6c0bee001')", "ObjectId('61bda13798857b6c0bee002')"]
},

{
    "_id": "ObjectId('61bc99c20ba2597e66a34221')",
    "nameVariant": "kaos Polos Hitam",
    "color": "Hitam",
    "qty": 12,
    "price": 99000
},

{
    "_id": "ObjectId('61bc99c20ba2597e66a34222')",
    "nameVariant": "kaos Polos Navy",
    "color": "Navy",
    "qty": 10,
    "price": 99000
}
```

4. Buatlah skema untuk kebutuhan data dari suatu aplikasi bioskop bernama SkilFlix. Data yang ingin ditampilkan adalah List Bioskop pada suatu Kota dan Film yang ditayangkan pada Setiap Bioskop tersebut. Jelaskan juga relasi apakah yang tepat untuk data tersebut?
Contoh Data yang dibutuhkan:
Cinemas
First Cinema
    Cinema Name: CGF
    Films:
        Venom 2
        Spiderman No Way Home
    Location: Pondok Indah Mall
Second Cinema
    Cinema Name: Cinema31
    Films:
        Venom 2
        Spiderman No Way Home
    Location: Mall Kelapa Gading
Jawab :Relasi yang tepat adalah one to one
**Skema**:
```json
{
    "_id": "ObjectId(61bc99c20ba2597e66a34223)",
    "cinemaName": "Cinema31",
    "films": ["Venom 2", "Spiderman No Way Home"],
    "location": "Pondok Indah Mall"
},

{
    "_id": "ObjectId(61bc99c20ba2597e66a34224)",
    "cinemaName": "CGF",
    "films": ["Venom 2", "Spiderman No Way Home"],
    "location": "Mall Kelapa Gading"
}
```
