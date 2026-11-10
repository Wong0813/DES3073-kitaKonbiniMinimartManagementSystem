# DES3073 - Kita Konbini Minimart Management System

[![PHP](https://img.shields.io/badge/PHP-8.2%2B-777BB4?logo=php)](https://www.php.net/)
[![Laravel](https://img.shields.io/badge/Laravel-11.x-FF2D20?logo=laravel)](https://laravel.com/)
[![MySQL](https://img.shields.io/badge/MySQL-Database-4479A1?logo=mysql)](https://www.mysql.com/)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

A full-featured Laravel-based minimart management system with a customer-facing storefront and an admin panel for managing products, inventory, and sales.

---

## 🛠 Tech Stack

- **Framework** — Laravel (PHP)
- **Frontend** — Blade Templates + Vanilla CSS / Tailwind CSS + JavaScript
- **Database** — MySQL (via Laragon / XAMPP)
- **Storage** — Laravel Storage (local disk)

---

## ✨ Features

### Customer Side
- Register & Login (Matric ID + Email)
- Browse & search products by category
- Shopping cart & checkout
- Wishlist
- Shelf locator — find product by shelf code
- Profile management

### Admin Panel
- Dashboard with stats, alerts & monthly sales chart
- Product management (CRUD + image upload)
- Inventory manager with batch tracking & expiry alerts
- Shelf management
- Category & user management
- Revenue report

---

## ⚙️ Setup & Installation

See **SETUP_GUIDE.txt** in this repo for full step-by-step setup instructions.

### Quick Start
```bash
# 1. Clone repository
git clone https://github.com/Wong0813/DES3073-kitaKonbiniMinimartManagementSystem.git
cd DES3073-kitaKonbiniMinimartManagementSystem

# 2. Install PHP & Node dependencies
composer install
npm install && npm run build

# 3. Environment configuration
cp .env.example .env
php artisan key:generate

# Configure your DB_DATABASE, DB_USERNAME, and DB_PASSWORD in .env

# 4. Run migrations and database seeder
php artisan migrate --seed

# 5. Link storage
php artisan storage:link

# 6. Start development server
php artisan serve
```

---

## 🔑 Default Login Credentials

| Role | Email | Password |
|------|-------|----------|
| Admin | admin@kitakonbini.com | admin123 |
| Demo User | demo@student.edu.my | password |

Admin panel: `/admin`

---

## 👥 Contributors

- d20231109113-art
- Yukariii123
- Aiman029
