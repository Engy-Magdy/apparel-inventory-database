<div align="center">

  <h1>👗 Clothing Store Inventory Database</h1>

  <p>A structured relational database project modeling a clothing store inventory using SQL and SQLite.</p>

  <!-- Badges -->
  <img src="https://img.shields.io/badge/Language-SQL-FFD700?style=for-the-badge&logo=sqlite&logoColor=black" alt="SQL Badge" />
  <img src="https://img.shields.io/badge/Database-SQLite-003B57?style=for-the-badge&logo=sqlite&logoColor=white" alt="SQLite Badge" />
  <img src="https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge" alt="Status Badge" />

  <br/><br/>

  ---

</div>

## 📌 Overview

This repository demonstrates foundational **Database Management** and **SQL querying** skills. It sets up a structured schema for a clothing store, populates inventory records, and performs analytical queries to inspect pricing and stock details.

---

## 🛠️ Key Concepts Applied

* **Data Definition Language (DDL):** Schema creation with data type constraints (`PRIMARY KEY`, `INTEGER`, `TEXT`).
* **Data Manipulation Language (DML):** Populating structured data with unique stock codes.
* **Data Retrieval & Sorting:** Ordering records using `ORDER BY`.
* **Aggregate Functions:** Analytical extraction using `MAX()` and `MIN()`.

---

## 📊 Database Schema (`clothes`)

| Column Name | Data Type | Key / Constraint | Description |
| :--- | :--- | :--- | :--- |
| **`id`** | `INTEGER` | `PRIMARY KEY` | Unique ID for each item |
| **`name`** | `TEXT` | — | Clothing category (e.g., Dress, Skirt, Shirt) |
| **`color`** | `TEXT` | — | Item color |
| **`price`** | `INTEGER` | — | Price of the item |
| **`code`** | `TEXT` | — | Unique stock identification code |

---

## 🗄️ SQL Queries & Script

```sql
-- 1. Create Table Schema
CREATE TABLE clothes (
    id INTEGER PRIMARY KEY,
    name TEXT,
    color TEXT,
    price INTEGER,
    code TEXT
);

-- 2. Insert Inventory Records
INSERT INTO clothes VALUES(1, 'Dress', 'White', 500, 'EN777');
INSERT INTO clothes VALUES(2, 'Dress', 'Red', 450, 'EN778');
-- ... [All records]

-- 3. Inventory Sorting & Price Analytics
SELECT * FROM clothes ORDER BY price;
SELECT name, color, code, MAX(price) FROM clothes;
SELECT name, color, code, MIN(price) FROM clothes;
