# 🌐 SocialBlog PHP

**SocialBlog PHP** adalah aplikasi platform blog sosial yang dibangun menggunakan **PHP Native (MVC)** dan **MySQL**. Aplikasi ini memungkinkan pengguna untuk mendaftar, membuat artikel maupun catatan pendek, serta berinteraksi (seperti komentar, *like*, *repost*, dan *bookmark*) dengan postingan dari pengguna lain.

---

## ✨ Fitur Utama

- **Autentikasi Pengguna**: Sistem Login dan Register yang aman (mendukung *multi-account switching*).
- **Manajemen Artikel & Postingan (CRUD)**: Pengguna dapat membuat, membaca, mengedit, dan menghapus artikel atau catatan pendek lengkap dengan *rich text editor* dan media.
- **Interaksi Sosial**: Fitur komentar, tombol suka (*Like*), *Repost*, *Bookmark*, tagar (*Explore Tags*), dan notifikasi.
- **Profil & Riwayat Pengguna**: Halaman khusus untuk melihat dan mengedit profil, daftar postingan pengguna, serta riwayat bacaan (*History*).
- **Responsif & Tema Gelap/Terang**: Antarmuka modern yang ramah pengguna dan dapat diakses dengan nyaman di perangkat *mobile* maupun *desktop* menggunakan **Tailwind CSS**.

---

## 🛠️ Teknologi yang Digunakan

- **Backend**: PHP Native (Arsitektur MVC)
- **Database**: MySQL / MariaDB
- **Frontend**: HTML5, CSS3, JavaScript
- **Framework CSS**: Tailwind CSS
- **Containerization**: Docker & Docker Compose (opsional)

---

## 🚀 Panduan Instalasi (Setup Lengkap)

Ikuti langkah-langkah di bawah ini untuk menjalankan project ini di `localhost` / komputer Anda.

### Prasyarat

Pastikan Anda sudah menginstal software berikut:
- **XAMPP**, **Laragon**, atau web server lokal lainnya (atau PHP Built-in Server / Docker).
- **PHP** versi 7.4 atau lebih baru (direkomendasikan PHP 8.x).
- **MySQL** / **MariaDB**.
- **Git** (opsional).

### Langkah-langkah

#### 1. Clone Repository
Buka terminal/CMD, arahkan ke folder `htdocs` (jika XAMPP) atau `www` (jika Laragon), lalu jalankan:

```bash
git clone https://github.com/Firrizq/socialblog-php.git
cd socialblog-php
```

#### 2. Konfigurasi Database
1. Buka **phpMyAdmin** (`http://localhost/phpmyadmin`).
2. Buat database baru dengan nama `ccit_socialblog` (atau sesuai nama database Anda).
3. Import file `.sql` database project ke dalam database yang baru dibuat.

#### 3. Konfigurasi Koneksi PHP
1. Salin file `app/config/config.example.php` menjadi `app/config/config.php`:
   ```bash
   cp app/config/config.example.php app/config/config.php
   ```
2. Buka file `app/config/config.php` dan sesuaikan detail koneksi dengan pengaturan lokal Anda:
   ```php
   <?php
   define('BASEURL', 'http://localhost:8000');
   define('DB_HOST', 'localhost');
   define('DB_USER', 'root'); // username database Anda
   define('DB_PASS', '');     // password database Anda (kosongkan jika default XAMPP)
   define('DB_NAME', 'ccit_socialblog'); // nama database
   ```

#### 4. Jalankan Aplikasi
- **Menggunakan PHP Built-in Server**:
  ```bash
  php -S localhost:8000 -t public
  ```
  Lalu buka browser dan akses: `http://localhost:8000`

- **Menggunakan XAMPP / Laragon**:
  Sesuaikan `BASEURL` di `app/config/config.php` menjadi `http://localhost/socialblog-php/public`, lalu akses URL tersebut di browser.

---

## 📸 Screenshots (Tangkapan Layar)

> *(Tambahkan tangkapan layar / screenshot aplikasi Anda di sini)*

| Halaman Beranda | Halaman Profil |
| :---: | :---: |
| ![Halaman Beranda](https://via.placeholder.com/600x350?text=Screenshot+Halaman+Beranda) | ![Halaman Profil](https://via.placeholder.com/600x350?text=Screenshot+Halaman+Profil) |

---

## 🤝 Kontribusi (Contributing)

Kontribusi selalu diterima! Jika Anda menemukan *bug* atau ingin menambahkan fitur baru:

1. **Fork** repository ini.
2. Buat *branch* fitur Anda:
   ```bash
   git checkout -b fitur-baru
   ```
3. *Commit* perubahan Anda:
   ```bash
   git commit -m "Menambahkan fitur baru"
   ```
4. *Push* ke *branch* tersebut:
   ```bash
   git push origin fitur-baru
   ```
5. Buka **Pull Request**.
