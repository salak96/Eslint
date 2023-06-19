# Eslint

# Eslint kita bisa memasang ESLint dengan menjalankan command berikut:
 
- npm install --save-dev eslint

- npm init @eslint/config

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

- npx eslint src

# Dalam file .eslintrc.json, kita bisa menambahkan peraturan ke "rules" seperti di bawah ini:

```
"rules": {
  "no-console": "warn"
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

# Jika kita menambahkan /* eslint-disable */ pada awal dari file, maka file akan dikecualikan dari peraturan ESLint.
- // eslint-disable-line bisa digunakan dalam baris yang sama:

```
if (text === 'hello') {
  console.log(text) // eslint-disable-line
}
```

# Cara lainnya adalah membuat file bernama .eslintignore dan membuat daftar file yang ingin kita matikan peraturannya.
- Buat file di root .eslintignore 

```
/node_modules
/src/App.tsx
*.tsx
```
