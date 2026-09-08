# SWIF — Warehouse Management System

**SWIF (Warehouse Management System)** is a web-based warehouse management application built with **Laravel 8** and **MySQL**. The system is designed to help warehouse staff manage inventory, monitor stock movements, process shipments, and maintain warehouse and administrator information through a centralized dashboard.

## Features

### 📊 Dashboard
- View current total inventory.
- Monitor monthly incoming stock.
- Monitor monthly outgoing stock.
- Display warehouse information.

### 📦 Inventory Management
- Add new inventory items.
- Edit existing inventory information.
- Delete inventory items.
- Organize items by category.
- Record item brand, supplier, stock quantity, and warehouse location.
- Prevent duplicate inventory based on brand and supplier.

### 🗂️ Inventory History
- Track inventory-related activities.
- Record stock additions, updates, and removals.
- Identify the administrator responsible for each activity.
- Review historical stock changes.

### 🚚 Shipment Management
- Create new shipment records.
- Automatically generate shipment invoice IDs.
- Record recipient information and delivery address.
- Track shipment quantities.
- Update shipment status.
- View shipment details.

### 👤 Administrator Management
- Administrator login and authentication.
- Add administrator accounts.
- Edit administrator information.
- Change administrator passwords.
- Delete administrator accounts.
- Manage administrator status.

### 🏢 Warehouse Management
- Store warehouse information.
- Update warehouse name, type, address, owner, and area.

---

## Tech Stack

| Technology | Usage |
|---|---|
| PHP | Backend programming language |
| Laravel 8 | Web application framework |
| MySQL | Database |
| Blade | Server-side templating |
| Laravel Sanctum | API authentication support |
| Laravel Mix | Frontend asset compilation |
| JavaScript | Frontend interactions |
| Bootstrap / Material Dashboard | UI components and styling |

## Requirements

Before installing SWIF, make sure your environment has:

- PHP **7.3 or higher**
- Composer
- MySQL
- Node.js and npm
- Git
- A local development environment such as XAMPP, Laragon, or Laravel Sail

> The project was developed using Laravel 8 and supports PHP `^7.3|^8.0` according to its `composer.json`.

---

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/Ryhnslmn13/SWIF.git
cd SWIF
```

### 2. Install PHP dependencies

```bash
composer install
```

### 3. Install frontend dependencies

```bash
npm install
```

### 4. Configure environment variables

Copy the example environment file:

```bash
cp .env.example .env
```

On Windows, you can also copy `.env.example` manually and rename the copy to `.env`.

Update the database configuration in `.env`:

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=swif
DB_USERNAME=root
DB_PASSWORD=
```

Create the corresponding MySQL database before running the migrations.

### 5. Generate the application key

```bash
php artisan key:generate
```

### 6. Run database migrations

```bash
php artisan migrate
```

If seed data is available and you want to populate the database:

```bash
php artisan db:seed
```

### 7. Compile frontend assets

For development:

```bash
npm run dev
```

For production:

```bash
npm run prod
```

### 8. Start the Laravel development server

```bash
php artisan serve
```

The application will normally be available at:

```text
http://127.0.0.1:8000
```

---

## Project Structure

```text
SWIF/
├── app/
│   ├── Console/
│   ├── Exceptions/
│   ├── Http/
│   │   ├── Controllers/
│   │   │   └── Auth/
│   │   │       ├── BarangController.php
│   │   │       ├── GudangController.php
│   │   │       ├── IntegratedController.php
│   │   │       ├── LoginController.php
│   │   │       ├── RegisterController.php
│   │   │       └── ShipmentController.php
│   │   └── Requests/
│   ├── Models/
│   └── Policies/
│
├── bootstrap/
├── config/
├── database/
│   ├── factories/
│   ├── migrations/
│   └── seeders/
│
├── public/
│   └── assets/
│
├── resources/
│   └── views/
│       ├── login.blade.php
│       ├── dashboard.blade.php
│       ├── barang.blade.php
│       ├── shipment.blade.php
│       ├── detailShipment.blade.php
│       ├── recordBarang.blade.php
│       └── admin.blade.php
│
├── routes/
│   ├── api.php
│   ├── web.php
│   └── console.php
│
├── .env.example
├── artisan
├── composer.json
└── package.json
```

---

## Development

Run the Laravel development server:

```bash
php artisan serve
```

Run Laravel Mix in development mode:

```bash
npm run dev
```

For automatic frontend asset rebuilding during development:

```bash
npm run watch
```

---

## Testing

The project uses PHPUnit through Laravel's testing framework.

Run the test suite with:

```bash
php artisan test
```

or:

```bash
./vendor/bin/phpunit
```

---

## Known Notes

This repository is a Laravel 8 application and contains some legacy/custom implementation choices in its database schema and controllers. If deploying the project to a new environment, verify the database migrations and configuration against the application's current models and controllers.

The application is primarily designed as a warehouse administration system rather than a public-facing e-commerce platform.

---

## Author

**SWIF Warehouse Management System**

GitHub Repository:  
https://github.com/Ryhnslmn13/SWIF
