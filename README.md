# 📚 Sistem Informasi Perpustakaan

Sistem Informasi Perpustakaan adalah aplikasi berbasis web yang dibangun menggunakan framework **Laravel**. Aplikasi ini dirancang untuk mengelola data perpustakaan secara efisien, meliputi manajemen data buku, penulis, penerbit, klasifikasi level, serta pencatatan aktivitas membaca/peminjaman oleh pengguna.

## ✨ Fitur Utama

Berdasarkan struktur arsitektur sistem, aplikasi ini memiliki beberapa fitur utama:
- **Manajemen Buku (CRUD):** Tambah, edit, hapus, dan lihat daftar buku.
- **Manajemen Entitas Perpustakaan:** Pengelolaan data *Author* (Penulis), *Publisher* (Penerbit), dan *Level* (Kategori/Tingkatan).
- **Pencatatan Aktivitas (Reads):** Sistem pencatatan riwayat membaca atau peminjaman buku.
- **Manajemen Pengguna & Hak Akses:** Otentikasi pengguna dengan pemisahan peran antara **Admin** dan **User** biasa.
- **Admin Dashboard:** Panel khusus admin untuk memantau dan mengelola keseluruhan data perpustakaan.

## 💻 Teknologi yang Digunakan

Proyek ini dikembangkan menggunakan *stack* modern:
- **Framework:** [Laravel](https://laravel.com/) (PHP)
- **Frontend Asset Bundler:** [Vite](https://vitejs.dev/)
- **Templating Engine:** Blade
- **Database:** MySQL / MariaDB (via Eloquent ORM)
- **JavaScript & CSS:** Diatur menggunakan `resources/js/app.js` dan dikompilasi oleh Vite.

## 📂 Struktur Direktori Utama

Berikut adalah gambaran arsitektur MVC (Model-View-Controller) pada proyek ini:
- `app/Models/` : Berisi model representasi database (`Book.php`, `Author.php`, `Publisher.php`, `Read.php`, `User.php`, `Admin.php`, `Level.php`).
- `app/Http/Controllers/` : Berisi logika bisnis dan pengendali aplikasi (`BookController.php`, `AuthorController.php`, `PublisherController.php`, dll).
- `database/migrations/` : Skema struktur tabel database untuk instalasi yang mudah.
- `resources/views/` : Antarmuka pengguna (UI) yang dibangun menggunakan Blade template (seperti `books/index.blade.php`, `admin/dashboard.blade.php`, dan `layouts/app.blade.php`).
- `routes/web.php` : Pusat pengaturan *routing* endpoint aplikasi web.

## 🚀 Persyaratan Sistem (Prerequisites)

Sebelum menjalankan proyek ini, pastikan sistem Anda telah terinstal:
- PHP >= 8.1
- [Composer](https://getcomposer.org/)
- [Node.js & NPM](https://nodejs.org/)
- Database MySQL / MariaDB

## 🛠️ Panduan Instalasi (Local Development)

Ikuti langkah-langkah berikut untuk menjalankan aplikasi ini di komputer lokal Anda:

1. **Clone Repository**
   ```bash
   git clone <url-repository-anda>
   cd perpustakaan

```

2. **Install Dependensi PHP (Composer)**
```bash
composer install

```


3. **Install Dependensi Frontend (NPM)**
```bash
npm install

```


4. **Konfigurasi Environment**
Salin file konfigurasi environment bawaan lalu sesuaikan kredensial database Anda.
```bash
cp .env.example .env

```


Buka file `.env` dan atur bagian database:
```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=nama_database_perpustakaan
DB_USERNAME=root
DB_PASSWORD=

```


5. **Generate Application Key**
```bash
php artisan key:generate

```


6. **Jalankan Migrasi & Seeder Database**
Perintah ini akan membuat tabel-tabel di database beserta data *dummy* awal (jika ada seeder).
```bash
php artisan migrate --seed

```


7. **Build Asset Frontend**
```bash
npm run build
# atau gunakan 'npm run dev' jika sedang dalam mode pengembangan (development)

```


8. **Jalankan Local Server**
```bash
php artisan serve

```



Aplikasi sekarang dapat diakses melalui browser pada alamat: `http://localhost:8000`

---

*Dibuat untuk keperluan manajemen Perpustakaan.*

```

```
