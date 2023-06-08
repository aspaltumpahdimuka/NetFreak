# Pages

## Auth
Kode di atas adalah komponen `Auth` yang digunakan dalam pengembangan web menggunakan Next.js dan Tailwind CSS. Mari kita jelaskan baris kode tersebut:

1. `import Input from "@/components/input";`: Mengimpor komponen `Input` dari direktori `@/components/input`. `@` adalah konfigurasi alias yang digunakan untuk merujuk ke direktori root dari proyek.

2. `import { useCallback, useState } from "react";`: Mengimpor hook `useCallback` dan `useState` dari pustaka React.

3. `const Auth = () => { ... }`: Mendefinisikan komponen `Auth` sebagai fungsi komponen (functional component) dengan menggunakan sintaksis arrow function.

4. `const [email, setEmail] = useState('')`: Mendeklarasikan state `email` menggunakan hook `useState`. State ini digunakan untuk menyimpan nilai email pengguna dan fungsi `setEmail` digunakan untuk memperbarui nilai state tersebut. Nilai awal state diinisialisasi sebagai string kosong.

5. `const [name, setName] = useState('')`: Mendeklarasikan state `name` menggunakan hook `useState`. State ini digunakan untuk menyimpan nilai nama pengguna dan fungsi `setName` digunakan untuk memperbarui nilai state tersebut. Nilai awal state diinisialisasi sebagai string kosong.

6. `const [password, setPassword] = useState('')`: Mendeklarasikan state `password` menggunakan hook `useState`. State ini digunakan untuk menyimpan nilai password pengguna dan fungsi `setPassword` digunakan untuk memperbarui nilai state tersebut. Nilai awal state diinisialisasi sebagai string kosong.

7. `const [variant, setVariant] = useState('login')`: Mendeklarasikan state `variant` menggunakan hook `useState`. State ini digunakan untuk menyimpan nilai variabel `variant` yang menunjukkan apakah pengguna sedang berada di mode 'login' atau 'register'. Fungsi `setVariant` digunakan untuk memperbarui nilai state tersebut. Nilai awal state diinisialisasi sebagai 'login'.

8. `const toggleVariant = useCallback(() => { ... })`: Mendefinisikan fungsi `toggleVariant` menggunakan hook `useCallback`. Fungsi ini digunakan untuk mengganti nilai `variant` antara 'login' dan 'register' ketika dipanggil. Fungsi ini memanfaatkan closure dan `currentVariant` untuk mendapatkan nilai saat ini dari `variant` dan memperbarui nilainya sesuai kondisi.

9. `return ( ... )`: Mengembalikan elemen JSX yang merupakan tampilan halaman autentikasi.

   - `<div className="relative h-full w-full bg-[url('/images/hero.jpg')] bg-no-repeat bg-center bg-fixed bg-cover"> ... </div>`: Menggunakan elemen div dengan kelas CSS "relative" untuk memuat latar belakang gambar pada halaman autentikasi. Properti "bg-[url('/images/hero.jpg')]" digunakan untuk menentukan gambar latar belakang.

   - `<div className="bg-black w-full h-full lg:bg-opacity-50"> ... </div>`: Menggunakan elemen div dengan kelas CSS "bg-black w-full h-full lg:bg-opacity-50" untuk menampilkan lapisan hitam semi-transparan di atas gambar latar belakang.

   - `<nav className="px-12 py-5"> ... </nav className="px-12 py-5"> ... </nav>`: Mendefinisikan elemen `nav` yang berisi logo. Properti kelas CSS "px-12 py-5" digunakan untuk memberikan padding horizontal dan vertical pada elemen `nav`.

   - `<img src="/images/logo.png" alt="Logo" className="h-12"/>`: Mendefinisikan elemen `img` yang menampilkan logo. Properti `src` digunakan untuk menentukan sumber gambar logo, `alt` digunakan untuk teks alternatif yang akan ditampilkan jika gambar gagal dimuat, dan kelas CSS "h-12" digunakan untuk menentukan tinggi gambar logo.

   - `<div className="flex justify-center"> ... </div>`: Menggunakan elemen div dengan kelas CSS "flex justify-center" untuk mengatur konten secara horizontal dan menerapkan penjajaran tengah secara horizontal.

   - `<div className="bg-black bg-opacity-10 px-16 py-16 self-center mt-2 lg:w-2/5 lg:max-w-md rounded-md w-full"> ... </div>`: Menggunakan elemen div dengan kelas CSS "bg-black bg-opacity-10 px-16 py-16 self-center mt-2 lg:w-2/5 lg:max-w-md rounded-md w-full" untuk memuat konten halaman autentikasi. Properti kelas CSS ini mengatur tampilan latar belakang, padding, lebar, dan bentuk elemen.

   - `<h2 className="text-white text-4xl mb-8 font-semibold"> ... </h2>`: Mendefinisikan elemen `h2` yang menampilkan teks judul "Masuk" atau "Daftar" tergantung pada nilai `variant`. Properti kelas CSS digunakan untuk mengatur tampilan teks, termasuk warna, ukuran, margin bawah, dan keberatan huruf.

   - `<div className="flex flex-col gap-4"> ... </div>`: Menggunakan elemen div dengan kelas CSS "flex flex-col gap-4" untuk mengatur tampilan elemen-elemen dalam kolom vertikal dengan jarak antar elemen yang ditentukan oleh properti kelas CSS "gap-4".

   - `{variant == 'register' && (...)}`: Menampilkan elemen Input hanya jika `variant` memiliki nilai 'register'.

   - `<Input ... />`: Menggunakan komponen `Input` dengan properti yang diperlukan. Properti `label` digunakan untuk menampilkan label input, properti `onChange` digunakan untuk menetapkan fungsi penangan perubahan input, properti `id` digunakan untuk menentukan ID input, dan properti `value` digunakan untuk menetapkan nilai input. Beberapa elemen `Input` ditampilkan dengan properti tambahan seperti `type` untuk menentukan tipe input.

   - `<button className="bg-red-600 py-3 text-white rounded-md w-full mt-10 hover:bg-red-700 transition"> ... </button>`: Mendefinisikan elemen `button` yang menampilkan teks "Masuk" atau "Daftar" tergantung pada nilai `variant`. Properti kelas CSS digunakan untuk mengatur tampilan tombol, termasuk warna latar belakang, padding, warna teks, bentuk tombol, lebar, margin atas, dan transisi saat dihover.

   - `<p className="text-neutral-500 mt-12">
        { variant == 'login' ? 'Pertama menggunakan NetFreak?' : 'Sudah punya akun.'}
            <span onClick={toggleVariant} className="
            text-white ml-1 hover:underline cursor-pointer
            ">
                {variant == 'login' ? 'Bikin akun' : 'Masuk'}
            </span>
        </p>: Menggunakan elemen `p` dengan kelas CSS "text-neutral-500 mt-12" untuk menampilkan teks "Pertama menggunakan NetFreak?" atau "Sudah punya akun." tergantung pada nilai `variant`. 

   - `<span onClick={toggleVariant} className="text-white ml-1 hover:underline cursor-pointer"> ... </span>`: Menggunakan elemen `span` dengan kelas CSS "text-white ml-1 hover:underline cursor-pointer" yang berisi teks "Bikin akun" atau "Masuk" tergantung pada nilai `variant`. Properti `onClick` digunakan untuk menetapkan fungsi `toggleVariant` saat pengguna mengklik teks.

10. `export default Auth;`: Mengekspor komponen `Auth` agar dapat digunakan di tempat lain dalam proyek.

Dengan menggunakan komponen `Auth` ini, Anda dapat membuat halaman autentikasi yang menampilkan input untuk email, nama (pada mode registrasi), dan kata sandi. Pengguna dapat beralih antara mode "login" dan "register" dengan mengklik teks yang sesuai. Tombol "Masuk" atau "Daftar" akan memicu tindakan sesuai dengan mode saat ini.