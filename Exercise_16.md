# 🎯 SQL Bolt — Exercise 16 (CREATE TABLE)

<p align="center">
  🏗️ Learn how to <b>create new tables</b> in SQL databases
</p>

---

## 📌 Overview

In this exercise, we learn how to:

* 🏗️ Create a new table
* 🧩 Define table schema
* 📊 Choose appropriate data types

Creating tables is the **foundation of database design**.

---

## 🧠 Concepts Covered

✔ CREATE TABLE
✔ Table schema
✔ Data types (TEXT, FLOAT, INTEGER)
✔ Column definition

---

## 📝 Exercise 16 — Task

Create a new table named **Database** with the following columns:

| Column Name    | Data Type | Description          |
| -------------- | --------- | -------------------- |
| Name           | TEXT      | Name of the database |
| Version        | FLOAT     | Latest version       |
| Download_count | INTEGER   | Number of downloads  |

---

## ✅ Solution

```sql id="g8d4ka"
CREATE TABLE Database (
    Name TEXT,
    Version FLOAT,
    Download_count INTEGER
);

```
<img width="916" height="586" alt="image" src="https://github.com/user-attachments/assets/b6ba3cfa-3b4a-4a64-813f-11bdaa53ed0d" />

---

## ⚙️ Syntax Used

```sql id="j5h9wd"
CREATE TABLE table_name (
    column1 datatype,
    column2 datatype,
    column3 datatype
);
```

---

## 📊 Explanation

* **TEXT** → stores string values (database name)
* **FLOAT** → stores decimal numbers (version)
* **INTEGER** → stores whole numbers (downloads)

---

## 🚀 How to Run

1. Open SQLBolt / MySQL / SQLite
2. Run the CREATE TABLE query
3. Verify using:

```sql id="n3p8zd"
SELECT name FROM sqlite_master WHERE type='table';
```

---

## 🌟 Features

✨ Beginner-friendly
✨ Core database concept
✨ Clean schema design
✨ GitHub portfolio ready

---

## 👨‍💻 Author

**Kunal Deshmukh**

---

## ⭐ Support

If this helped you:

⭐ Star the repository
🚀 Share with others
📘 Keep learning SQL

---

## 💬 Pro Tip

👉 Use `IF NOT EXISTS` to avoid errors:

```sql id="k9m2we"
CREATE TABLE IF NOT EXISTS Database (
    Name TEXT,
    Version FLOAT,
    Download_count INTEGER
);
```

---
