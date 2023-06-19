<!-- @format -->

# Prettier

# Untuk proses pemasangan Prettier dalam proyek kita, jalankan command berikut ini :

-   npm install --save-dev --save-exact prettier

# Kemudian buatlah file konfigurasi untuk Prettier dengan command ini:

```
echo {}> .prettierrc.json
```

# Ketika kita ingin menyesuaikan pengaturan default dari Prettier, kita bisa menambahkan opsi pada .prettierrc.json, misalnya:

```
{
  "printWidth": 120, // default: 80
  "semi": false, // default: true
  "singleQuote": true, // default: false
  "bracketSpacing": false // default true
}
```

# Ketika kita ingin menerapkan seluruh coding style dari Prettier sekaligus, jalankan command

-   npx prettier --write src

# Jika ingin mengabaikan peraturan Prettier, kita bisa melakukan yang sama terhadap ESLint.

-   // prettier-ignore comment untuk baris tertentu
-   .prettierignore untuk file atau folder tertentu

# Terdapat package bernama eslint-config-prettier dan itu mematikan semua peraturan yang tidak perlu atau bahkan konflik dengan Prettier.

-   Jalankan command berikut ini untuk memulai proses pemasangan:

```
npm install --save-dev eslint-config-prettier
```

# Sudah siap setelah menambahkan "prettier" ke "extends" dari .eslintrc.json.

```
{
  "extends": [
    "other-configs",
    "prettier"
  ]
}
```

# Cara lainnya untuk menambah di package json copy comant

-   edit package json . di script tambahkan

```

"format": "prettier --write .",

```
