<!-- @format -->

# Eslint

# Eslint kita bisa memasang ESLint dengan menjalankan command berikut:

-   npm install --save-dev eslint

-   npm init @eslint/config

# Buat .eslintrc.json diroot jika sudah ada tinggal edit

```
{
    "env": {
        "browser": true,
        "es2021": true
    },
    "extends": [
        "plugin:react/recommended",
        "standard-with-typescript"
    ],
    "overrides": [
    ],
    "parserOptions": {
        "ecmaVersion": "latest",
        "sourceType": "module",
        "project": "./tsconfig.json" // Silahkan tambahkan ini sendiri
    },
    "plugins": [
        "react"
    ],
    "rules": {
    }
}
```

# Jika ESLint sudah terpasang dengan baik, kita bisa melihat error ketika menjalankan command npx eslint file_path:

-   npx eslint src

# Dalam file .eslintrc.json, kita bisa menambahkan peraturan ke "rules" seperti di bawah ini:

```
"rules": {
  "no-console": "warn"
  }
```

# Untuk mematikan peraturan pada baris tertentu, kita bisa menambahkan comment seperti eslint-disable-next-line rule-name:

```
if (text === 'hello') {
  // eslint-disable-next-line no-console
  console.log(text)
}
```

# Terdapat pola untuk membuat comment seperti ini:

```
/* eslint-disable */
// eslint-disable-next-line
// eslint-disable-line
```

# Jika kita menambahkan /_ eslint-disable _/ pada awal dari file, maka file akan dikecualikan dari peraturan ESLint.

-   // eslint-disable-line bisa digunakan dalam baris yang sama:

```
if (text === 'hello') {
  console.log(text) // eslint-disable-line
}
```

# Cara lainnya adalah membuat file bernama .eslintignore dan membuat daftar file yang ingin kita matikan peraturannya.

-   Buat file di root .eslintignore

```
/node_modules
/src/App.tsx
*.tsx
```

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
