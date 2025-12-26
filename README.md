# AccountingCore
### Inventory & Accounting Engine (Laravel)

> AccountingCore is a production-grade inventory accounting engine that provides transactional stock control through document-based operations and rule validation.
---

## 🚀 What Is AccountingCore

AccountingCore is a backend accounting engine built on Laravel that implements real inventory bookkeeping logic rather than simple item CRUD.
It uses accounting documents (Bills) and rule-validated operations to control all stock movements, ensuring balance integrity, transactional safety, and audit-ready data structures.
It is designed to serve as the core backend layer for POS systems, warehouses, shops, cafes, service centers, and ERP microservices.

---

## 🎯 Who This Is For

- POS systems
- Warehouses
- Shops
- Cafes & restaurants
- ERP microservices
- Fulfillment services

---

## ⚙️ Tech Stack

| Layer | Stack |
|------|------|
| Backend | Laravel |
| Language | PHP 8+ |
| Database | MySQL / PostgreSQL |
| API Docs | OpenAPI / Swagger |
| Tests | PHPUnit |

---

## 🧠 Core Accounting Model

<pre>Product → Bill → BillItem → Book → BookBalance
                        ↓
                OperationType + Rules</pre>


---

## 🧱 Domain Concepts

| Entity | Description |
|-------|------------|
| Product |Any inventory item|
| Book |Warehouse / accounting book|
| Bill |Accounting document|
| BillItem |Line inside a bill|
| BookBalance |Calculated stock balances|
| OperationType |Type of stock operation|
| OperationTypeRule |Rule engine controlling operations|

---

## ⚡ Quick Start

```bash
composer install
cp .env.example .env
php artisan key:generate
php artisan migrate
php artisan serve
```

## 📘 API Documentation

OpenAPI.yaml

OpenApiResolved.json

## 🌐 API Overview

| Endpoint | Method | Description
|----------|------------|--------|
|/api/products|GET|List products
|/api/products|POST|Create product
|/api/books|GET|List warehouses / books
|/api/books|POST|Create warehouse / book
|/api/operation-types|GET|List operation types
|/api/operation-types|POST|Create operation type
|/api/bills|POST|Create accounting document
|/api/bills/{id}|GET|Get bill details
|/api/bills/{id}/items|POST|Add bill line
|/api/bills/{id}/commit|POST|Commit bill and update balances
|/api/balances|GET|Get current stock balances
## 🛡 Business Guarantees

Guarantee

- Negative stock protection<br>
- Transactional commits<br>
- Rule-based operations<br>
- OpenAPI contract<br>
- Automated tests<br>

## 🧩 Extensibility

- Multi-warehouse<br>
- FIFO / LIFO<br>
- Batches & expiration<br>
- Reservations<br>
- Financial valuation<br>
- Multi-currency<br>
- Audit logs<br>
- Webhooks<br>

🏁 Production Checklist

- Docker Compose
- CI/CD
- RBAC
- Audit logs
