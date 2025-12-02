# ☕ Website Cafe Friendzone

<div align="center">

![Laravel](https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-54. 7%25-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Bootstrap](https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white)
![Vite](https://img.shields. io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)

**Platform Website Modern untuk Cafe Friendzone**

[Demo](#demo) • [Fitur](#-fitur) • [Instalasi](#-instalasi) • [Dokumentasi](#-dokumentasi)

</div>

---

## 📖 Tentang Proyek

Website Cafe Friendzone adalah platform web modern yang dibangun dengan Laravel untuk mengelola operasional cafe. Aplikasi ini menyediakan interface yang user-friendly untuk pelanggan dan sistem manajemen yang powerful untuk administrator.

## ✨ Fitur

### 🎯 Untuk Pelanggan
- 🏠 **Landing Page Menarik** - Tampilan homepage yang eye-catching
- 📋 **Menu Digital** - Katalog menu lengkap dengan gambar dan harga
- 🛒 **Sistem Pemesanan Online** - Pesan menu favorit dengan mudah
- 📱 **Responsive Design** - Optimal di semua perangkat
- 🔍 **Pencarian Menu** - Temukan menu yang Anda inginkan dengan cepat

### 👨‍💼 Untuk Administrator
- 📊 **Dashboard Admin** - Monitoring aktivitas cafe real-time
- 🍔 **Manajemen Menu** - CRUD menu dengan mudah
- 📦 **Manajemen Pesanan** - Kelola pesanan pelanggan
- 👥 **Manajemen User** - Kontrol akses pengguna
- 📈 **Laporan & Analitik** - Insight bisnis yang mendalam

## 🛠️ Teknologi yang Digunakan

| Kategori | Teknologi |
|----------|-----------|
| **Backend Framework** | Laravel (PHP) |
| **Frontend** | JavaScript (54.7%), HTML, Blade Templates |
| **Styling** | CSS (25.9%), SCSS (12.9%), Less (1.4%), Bootstrap 5 |
| **Build Tool** | Vite 4.0 |
| **Package Manager** | Composer, NPM |
| **Icons** | Unicons |
| **HTTP Client** | Axios |

## 📁 Struktur Proyek

```
Website-Cafe-Friendzone/
└── Friendzone/
    ├── app/                    # Logic aplikasi (Models, Controllers, Middleware)
    ├── bootstrap/              # Bootstrap framework
    ├── config/                 # File konfigurasi
    ├── database/               # Migrations, Seeders, Factories
    ├── public/                 # Assets public (CSS, JS, Images)
    │   └── admin-assets/       # Assets untuk admin panel
    ├── resources/              # Views, SCSS, JS source files
    │   ├── views/              # Blade templates
    │   ├── css/                # CSS/SCSS files
    │   └── js/                 # JavaScript files
    ├── routes/                 # Route definitions (web, api)
    ├── storage/                # Logs, cache, uploaded files
    ├── tests/                  # Unit & Feature tests
    ├── . env. example            # Environment variables template
    ├── artisan                 # CLI tool Laravel
    ├── composer.json           # PHP dependencies
    ├── package.json            # NPM dependencies
    └── vite.config.js          # Vite configuration
```

## 🚀 Instalasi

### Prasyarat

Pastikan sistem Anda telah terinstall:
- PHP >= 8.1
- Composer
- Node.js & NPM
- MySQL / PostgreSQL / SQLite
- Web Server (Apache / Nginx)

### Langkah Instalasi

1.  **Clone Repository**
   ```bash
   git clone https://github.com/christian050104/Website-Cafe-Friendzone.git
   cd Website-Cafe-Friendzone/Friendzone
   ```

2.  **Install Dependencies PHP**
   ```bash
   composer install
   ```

3. **Install Dependencies JavaScript**
   ```bash
   npm install
   ```

4.  **Konfigurasi Environment**
   ```bash
   cp .env.example .env
   php artisan key:generate
   ```

5. **Konfigurasi Database**
   
   Edit file `.env` dan sesuaikan dengan database Anda:
   ```env
   DB_CONNECTION=mysql
   DB_HOST=127.0.0.1
   DB_PORT=3306
   DB_DATABASE=cafe_friendzone
   DB_USERNAME=root
   DB_PASSWORD=
   ```

6. **Migrasi Database**
   ```bash
   php artisan migrate
   ```

7.  **Seed Database (Opsional)**
   ```bash
   php artisan db:seed
   ```

8. **Generate Storage Link**
   ```bash
   php artisan storage:link
   ```

## 💻 Menjalankan Aplikasi

### Development Mode

Buka 2 terminal terpisah:

**Terminal 1 - Laravel Server:**
```bash
php artisan serve
```

**Terminal 2 - Vite Dev Server:**
```bash
npm run dev
```

Aplikasi akan berjalan di: `http://localhost:8000`

### Production Mode

1. **Build Assets:**
   ```bash
   npm run build
   ```

2. **Optimize Laravel:**
   ```bash
   php artisan config:cache
   php artisan route:cache
   php artisan view:cache
   ```

3.  **Setup Web Server**
   
   Arahkan document root ke folder `public/`

## 🔧 Konfigurasi

### Environment Variables Penting

```env
APP_NAME="Cafe Friendzone"
APP_ENV=local
APP_DEBUG=true
APP_URL=http://localhost

# Database
DB_CONNECTION=mysql
DB_DATABASE=cafe_friendzone

# Mail (untuk notifikasi)
MAIL_MAILER=smtp
MAIL_HOST=smtp.gmail.com
MAIL_PORT=587

# Storage (jika menggunakan cloud storage)
AWS_ACCESS_KEY_ID=
AWS_SECRET_ACCESS_KEY=
AWS_DEFAULT_REGION=
```

## 📚 Dokumentasi

### Artisan Commands

```bash
# Lihat semua routes
php artisan route:list

# Clear cache
php artisan cache:clear
php artisan config:clear
php artisan view:clear

# Membuat controller
php artisan make:controller NamaController

# Membuat model dengan migration
php artisan make:model NamaModel -m

# Menjalankan tests
php artisan test
```

### NPM Scripts

```bash
# Development dengan hot reload
npm run dev

# Build untuk production
npm run build

# Watch mode untuk development
npm run watch
```

## 🎨 Customization

### Mengubah Tema

1. Edit file SCSS di `resources/sass/`
2. Sesuaikan variabel Bootstrap di `resources/sass/_variables.scss`
3.  Rebuild assets: `npm run build`

### Menambah Menu Baru

1. Buat migration: `php artisan make:migration create_menus_table`
2.  Buat model: `php artisan make:model Menu`
3. Buat controller: `php artisan make:controller MenuController`
4. Tambahkan routes di `routes/web.php`

## 🧪 Testing

```bash
# Run all tests
php artisan test

# Run specific test
php artisan test --filter TestClassName

# Run with coverage
php artisan test --coverage
```

## 📦 Dependencies

### PHP Dependencies (composer.json)
- Laravel Framework
- Laravel UI / Breeze / Jetstream (tergantung implementasi)
- Intervention Image (untuk image processing)

### JavaScript Dependencies (package.json)
- **Bootstrap 5. 2. 3** - CSS Framework
- **Axios 1.1.2** - HTTP Client
- **@popperjs/core 2.11.6** - Tooltip & Popover
- **Vite 4.0.0** - Build Tool
- **Sass 1.56.1** - CSS Preprocessor

## 🚀 Deployment

### Deploy ke Shared Hosting

1. Upload semua file kecuali `node_modules` dan `vendor`
2. Run `composer install --optimize-autoloader --no-dev`
3. Run `npm run build`
4.  Set document root ke `/public`
5. Set permissions untuk `/storage` dan `/bootstrap/cache`

### Deploy ke VPS (Ubuntu)

```bash
# Install dependencies
sudo apt update
sudo apt install php8.1-fpm php8.1-mysql nginx mysql-server

# Setup Laravel
cd /var/www/cafe-friendzone
composer install --optimize-autoloader --no-dev
npm run build

# Configure Nginx
sudo nano /etc/nginx/sites-available/cafe-friendzone

# Setup SSL dengan Let's Encrypt
sudo certbot --nginx -d yourdomain.com
```

## 🤝 Kontribusi

Kontribusi sangat diterima! Untuk berkontribusi:

1. Fork repository ini
2. Buat branch fitur baru (`git checkout -b feature/AmazingFeature`)
3.  Commit perubahan (`git commit -m 'Add some AmazingFeature'`)
4. Push ke branch (`git push origin feature/AmazingFeature`)
5.  Buat Pull Request

### Coding Standards

- Follow PSR-12 untuk PHP
- Use ESLint untuk JavaScript
- Write tests untuk fitur baru
- Update dokumentasi jika diperlukan

## 🐛 Bug Report

Temukan bug?  Silakan buat issue dengan detail:
- Deskripsi bug
- Langkah reproduksi
- Expected behavior
- Screenshots (jika ada)
- Environment (OS, Browser, PHP version)

## 📝 Changelog

### Version 1.0.0
- ✅ Initial release
- ✅ Landing page
- ✅ Menu management
- ✅ Order system
- ✅ Admin dashboard

## 📄 Lisensi

Proyek ini bersifat open source dan dapat digunakan untuk keperluan pembelajaran dan pengembangan.

## 👨‍💻 Developer

**christian050104**
- GitHub: [@christian050104](https://github.com/christian050104)

## 🙏 Acknowledgments

- Laravel Community
- Bootstrap Team
- Iconscout untuk Unicons
- Semua kontributor yang telah membantu proyek ini

## 📞 Support

Butuh bantuan? Hubungi kami melalui:
- 📧 Email: [Create an issue](https://github.com/christian050104/Website-Cafe-Friendzone/issues)
- 💬 Discussions: [GitHub Discussions](https://github.com/christian050104/Website-Cafe-Friendzone/discussions)

## 🌟 Show Your Support

Berikan ⭐ jika proyek ini bermanfaat! 

---

<div align="center">

**Made with ☕ and ❤️ by christian050104**

[⬆ Back to Top](#-website-cafe-friendzone)

</div>
```
