# Components

## Input
Kode di atas adalah komponen Input yang digunakan dalam pengembangan web menggunakan Next.js dan Tailwind CSS. Mari kita jelaskan baris kode tersebut:

1. `import React from "react"`: Mengimpor pustaka React yang diperlukan untuk membuat komponen React.

2. `interface InputProps { ... }`: Mendefinisikan sebuah interface TypeScript bernama InputProps. Interface ini mendefinisikan properti-properti yang diperlukan oleh komponen Input.

   - `id: string`: Properti yang mewakili ID input.
   - `onChange: any`: Properti yang mewakili fungsi penangan perubahan input.
   - `value: string`: Properti yang mewakili nilai input.
   - `label: string`: Properti yang mewakili label input.
   - `type?: string`: Properti opsional yang mewakili tipe input.

3. `const Input: React.FC<InputProps> = ({ ... }) => { ... }`: Mendefinisikan komponen Input sebagai fungsi komponen (functional component) dengan menggunakan sintaksis arrow function. Komponen ini menerima properti-properti yang didefinisikan oleh InputProps.

4. `return ( ... )`: Mengembalikan elemen JSX yang berisi tampilan input dan label.

   - `<div className="relative"> ... </div>`: Menggunakan elemen div dengan kelas CSS "relative" untuk memuat elemen input dan label.

   - `<input ... />`: Mendefinisikan elemen input. Properti-properti yang diberikan adalah:
     - `onChange={onChange}`: Menentukan fungsi penangan perubahan input.
     - `id={id}`: Menentukan ID input.
     - `type={type}`: Menentukan tipe input. Properti ini bersifat opsional.
     - `value={value}`: Menentukan nilai input.
     - `className=" ... "`: Mendefinisikan kelas-kelas CSS untuk mengatur tampilan input menggunakan Tailwind CSS.
     - `placeholder=" "`: Menetapkan placeholder kosong untuk input.

   - `<label ... > ... </label>`: Mendefinisikan elemen label yang berkaitan dengan input.
     - `className=" ... "`: Mendefinisikan kelas-kelas CSS untuk mengatur tampilan label menggunakan Tailwind CSS.
     - `htmlFor={id}`: Mengaitkan label dengan input menggunakan ID input.
     - `{label}`: Menampilkan teks label.

5. `export default Input;`: Mengekspor komponen Input agar dapat digunakan di tempat lain dalam proyek.

Dengan menggunakan komponen Input ini, Anda dapat membuat input form dengan label yang terintegrasi dengan gaya desain menggunakan Tailwind CSS.
