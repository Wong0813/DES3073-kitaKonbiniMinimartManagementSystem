# DES3073 - Kita Konbini Minimart Management System / 便利店综合管理系统

[![PHP](https://img.shields.io/badge/PHP-8.1%2B-777BB4?logo=php)](https://www.php.net/)
[![Laravel](https://img.shields.io/badge/Laravel-10.x-FF2D20?logo=laravel)](https://laravel.com/)
[![MySQL](https://img.shields.io/badge/MySQL-Database-4479A1?logo=mysql)](https://www.mysql.com/)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

[English](#english) | [中文说明](#chinese)

---

<a name="english"></a>
## 🌐 English

### Project Overview
**Kita Konbini Minimart Management System** is a full-featured web-based retail and e-commerce application developed for the **DES3073** course. Modeled after modern Japanese-style convenience stores (*Konbini*), the system streamlines store operations, inventory management, customer purchasing workflows, and online promotional campaigns.

### Key Features
* **User Authentication & Authorization**:
  * Secure user registration, authentication, profile management, and password recovery.
  * Role-based views separating administrative controls and shopper experiences.
* **Product & Category Management**:
  * Comprehensive CRUD operations for store items, categories, and inventory tracking.
  * Shelf positioning system (`ShelfController`) to map physical and digital shelf stocking.
* **Shopping Cart & Ordering**:
  * Dynamic shopping cart (`CartController`) supporting item quantity adjustments, instant subtotal calculation, and checkout workflows.
* **Storefront & Promotions**:
  * Responsive homepage banner carousel (`promo_banner`) highlighting daily deals and featured snacks/beverages.
  * Database seeders preloaded with convenience store product catalogues.

### Tech Stack
* **Backend Framework:** Laravel 10 (PHP 8.1+)
* **Database & ORM:** MySQL / SQLite with Eloquent ORM
* **Frontend:** Laravel Blade Templates, Custom CSS / Tailwind CSS, JavaScript
* **Security:** CSRF protection, password hashing (bcrypt), input validation

### Architecture & Key Components
```text
├── app/
│   ├── Http/Controllers/
│   │   ├── AuthController.php      # User login, registration & session lifecycle
│   │   ├── CartController.php      # Shopping cart operations & order calculations
│   │   ├── HomeController.php      # Storefront & promotional display
│   │   ├── ProductController.php   # Product listings, filtering & details
│   │   ├── ProfileController.php   # User profile settings
│   │   └── ShelfController.php     # In-store shelf & inventory organization
│   └── Models/
│       ├── Category.php            # Product categorization model
│       ├── Product.php             # Merchandise data & stock attributes
│       └── User.php                # User credentials & account details
├── database/
│   └── seeders/DatabaseSeeder.php  # Automated test data & product seeder
└── resources/views/                # Blade layout templates, auth & store pages
```

### Installation & Setup

#### Prerequisites
* PHP >= 8.1 with OpenSSL, PDO, Mbstring, and Tokenizer extensions
* [Composer](https://getcomposer.org/)
* MySQL / MariaDB (or SQLite for local testing)

#### Quick Start
```bash
# 1. Clone repository
git clone https://github.com/Wong0813/DES3073-kitaKonbiniMinimartManagementSystem.git
cd DES3073-kitaKonbiniMinimartManagementSystem

# 2. Install PHP dependencies
composer install

# 3. Environment configuration
cp .env.example .env
php artisan key:generate

# Configure your DB_DATABASE, DB_USERNAME, and DB_PASSWORD in .env

# 4. Run migrations and database seeder
php artisan migrate --seed

# 5. Start development server
php artisan serve
```
Access the application at `http://127.0.0.1:8000`.

---

<a name="chinese"></a>
## 🇨🇳 中文说明

### 项目简介
**Kita Konbini 便利店管理系统** 是在 **DES3073 课程** 中完成的 Web 商业应用系统。项目以日式便利店（Konbini）经营模式为蓝本，构建了集商品陈列、库存货架维护、顾客在线选购、购物车结算及营销促销于一体的综合零售系统。

### 核心功能
* **身份认证与权限管理**：支持用户注册、登录、个人资料管理及密码重置，内置完善的数据验证与加密保护。
* **商品与品类管理**：商品信息的增删改查，支持分类归属与物理/虚拟货架分布管理（`ShelfController`）。
* **购物车与结算流程**：支持实时添加商品、加减数量、库存联动与订单总额计算。
* **营销活动展示**：首页集成促销横幅与特惠商品展示，支持数据库 Seeder 一键导入预设便利店商品库。

### 技术栈
* **后端框架：** Laravel 10 (PHP 8.1+)
* **数据库：** MySQL / SQLite + Eloquent ORM
* **前端展示：** Blade 模板引擎、响应式 CSS
* **安全特性：** CSRF 防护、Bcrypt 密码哈希、参数过滤验证
