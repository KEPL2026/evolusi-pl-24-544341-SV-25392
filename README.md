# Evolusi PL — Goal Tracker

Aplikasi web sederhana berbasis **Laravel** untuk mencatat dan mengelola goals/tujuan pribadi.

Dibuat sebagai tugas praktikum **Evolusi Perangkat Lunak** — KEPL2026.

---

## 📋 Fitur

- Menampilkan daftar goal dari database
- Tambah goal baru melalui form
- Hapus goal yang sudah selesai
- Validasi input di sisi server

---

## 🛠️ Teknologi

- **PHP 8.4** + **Laravel 12**
- **SQLite** (development) / MySQL (production)
- **Blade** templating engine
- **GitHub Actions** CI (Lint + Test)

---

## 🚀 Menjalankan di Lokal

### Prasyarat

Pastikan sudah terinstal:
- PHP >= 8.2
- Composer
- Node.js & npm (opsional, untuk asset)

### Langkah-langkah

```bash
# 1. Clone repository
git clone https://github.com/KEPL2026/evolusi-pl-24-544341-SV-25392.git
cd evolusi-pl-24-544341-SV-25392

# 2. Install dependensi PHP
composer install

# 3. Salin file environment
cp .env.example .env

# 4. Generate app key
php artisan key:generate

# 5. Buat file database SQLite
touch database/database.sqlite

# 6. Jalankan migrasi
php artisan migrate

# 7. Jalankan server lokal
php artisan serve
```

Akses aplikasi di: **http://localhost:8000**

---

## 🧪 Menjalankan Tests

```bash
php artisan test
```

---

## 🏗️ Struktur Branch

```
main        ← production (protected)
└── dev     ← staging/development (protected)
    └── feature/goal-tracker  ← fitur yang dikerjakan
```

**Alur kerja:**
1. Buat branch `feature/<nama>` dari `dev`
2. Kerjakan fitur, lalu buka PR: `feature` → `dev`
3. Setelah review, buka PR: `dev` → `main`
4. Tidak ada push langsung ke `main` atau `dev`

---

## ⚙️ CI/CD

GitHub Actions berjalan otomatis pada setiap push dan pull request:

| Job | Deskripsi |
|-----|-----------|
| **Lint** | Cek code style dengan Laravel Pint |
| **Test** | Jalankan PHPUnit test suite |

---

## 📁 Struktur Proyek

```
app/
├── Http/Controllers/GoalController.php   ← Controller utama
├── Models/Goal.php                        ← Eloquent model
database/
├── migrations/                            ← Skema database
resources/views/
├── goals/index.blade.php                  ← Tampilan utama
routes/
├── web.php                                ← Definisi routes
.github/workflows/
├── ci.yml                                 ← GitHub Actions CI
```

---

## 👤 Identitas

- **Nama:** Gurveenderjeet Kaur
- **NIM:** 24/544341/SV/25392
- **Mata Kuliah:** Evolusi Perangkat Lunak 
