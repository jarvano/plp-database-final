# E-commerce Database Schema (MySQL)

This project contains a **complete relational database schema** for an E-commerce Store, implemented in **MySQL**.  
It is designed for a Database Management Systems (DBMS) assignment and demonstrates proper database design principles, normalization, and relationship modeling.

---

## 🎯 Objective

To design and implement a **full-featured relational database** for an online store that manages:

- Users and Customers
- Products, Categories, and Inventory
- Orders, Order Items, and Payments
- Reviews and Coupons
- Addresses and Suppliers

---

## 📂 Deliverables

- **ecommerce_schema.sql**  
  Contains:
  - `CREATE DATABASE` statement
  - `CREATE TABLE` statements with constraints
  - Primary and Foreign Keys
  - One-to-One, One-to-Many, and Many-to-Many relationships
  - Views and indexes for performance

---

## 🏗️ Database Design

### Relationships

- **One-to-One:**  
  - `users` ↔ `customers` (one user has one customer profile)

- **One-to-Many:**  
  - `customers` → `addresses`  
  - `orders` → `order_items`  
  - `orders` → `payments`  

- **Many-to-Many:**  
  - `products` ↔ `categories` (via `product_categories`)  
  - `orders` ↔ `coupons` (via `order_coupons`)

### Normalization

- Schema follows **1NF, 2NF, and 3NF** to eliminate redundancy and maintain data integrity.
- Includes `NOT NULL`, `UNIQUE`, and `CHECK` constraints.

---

## ⚙️ Setup Instructions

1. Install **MySQL** on your system.
2. Open **MySQL CLI** or **Workbench**.
3. Run the schema file:

```sql
SOURCE /path/to/ecommerce_schema.sql;
