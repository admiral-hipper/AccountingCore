# FridgeMaster — Inventory & Accounting Engine

FridgeMaster is a Laravel-based REST backend that implements a **real inventory/accounting engine**.
It supports stock balances, operation rules, and transactional movements — not just CRUD.

Can be used as a core for:
- Warehouse systems
- Shops / POS
- Cafes & restaurants
- Spare parts accounting
- Fulfillment services

## Tech
- Laravel
- PHP 8+
- OpenAPI (Swagger)
- PHPUnit

## Core Concepts

| Concept | Description |
|-------|-------------|
| Product | Any stock item |
| Book | Accounting book (main storage) |
| Bill | Accounting document |
| BillItem | Item line in a bill |
| BookBalance | Calculated stock balances |
| OperationType | Type of operation (income, outcome, etc.) |
| OperationTypeRule | Rules that control allowed operations |

## Quick Start

```bash
composer install
cp .env.example .env
php artisan key:generate
php artisan migrate
php artisan serve

```
# API Docs

## OpenAPI specs:

OpenAPI.yaml

OpenApiResolved.json

Import into Postman / Swagger UI.

# Tests
php artisan test

# Use Cases

- Inventory management systems
- POS backends
- Warehouse automation
- Cafe / Restaurant stock systems
- ERP microservices

