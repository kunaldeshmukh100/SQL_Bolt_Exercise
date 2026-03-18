# 🎯 SQL Bolt — Exercise 7 (OUTER JOINs)

<p align="center">
  🏢 Master SQL using <b>LEFT JOIN</b> to handle missing data
</p>

---

## 📌 Overview

This exercise introduces **OUTER JOINs**, specifically the `LEFT JOIN`.

You will learn how to:

* 🔗 Combine tables even when data is missing
* 🏢 Include all records from one table
* ⚠️ Handle `NULL` values
* 👨‍💼 Analyze employee distribution across buildings

---

## 🧠 Concept: LEFT JOIN

```sql
SELECT column1, column2
FROM table1
LEFT JOIN table2
ON table1.id = table2.id;
```

💡 A `LEFT JOIN` returns **all rows from the left table**, and matching rows from the right table.
If no match exists → result will contain **NULL values**

---

## 📊 Tables Used

### 🏢 Buildings Table

* building_name
* capacity

### 👨‍💼 Employees Table

* name
* role
* building

---

# 📝 Exercise 7 — Solutions

---

## 🔹 1. Find the list of all buildings that have employees

```sql
SELECT DISTINCT building_name
FROM employees;
```

💡 Returns only buildings that currently have employees

---

## 🔹 2. Find the list of all buildings and their capacity

```sql
SELECT building_name, capacity
FROM buildings;
```

💡 Includes all buildings (even empty ones)

---

## 🔹 3. List all buildings and the distinct employee roles (including empty buildings)

```sql
SELECT DISTINCT buildings.building_name, employees.role
FROM buildings
LEFT JOIN employees
ON buildings.building_name = employees.building
ORDER BY buildings.building_name;
```

💡

* Keeps all buildings
* Shows roles if present
* Shows `NULL` for empty buildings

---

## ⚙️ Key Concepts Used

| Concept   | Description                       |
| --------- | --------------------------------- |
| LEFT JOIN | Includes all rows from left table |
| DISTINCT  | Removes duplicate values          |
| NULL      | Represents missing data           |
| ORDER BY  | Sorts results                     |

---

## 🚀 How to Run

```bash
1. Open SQLBolt or any SQL tool
2. Copy the queries
3. Execute them
4. Observe how missing data appears as NULL
```

---

## 🌟 Features

✨ Outer join queries
✨ Handles missing data
✨ Real-world scenario (empty buildings)
✨ Beginner-friendly explanation

---

## 👨‍💻 Author

**Kunal Deshmukh**

---

## ⭐ Support

If you found this helpful:

* ⭐ Star the repository
* 🔁 Share with friends
* 🚀 Keep learning SQL

---

## 💬 Pro Tip

```sql
LEFT JOIN
```

👉 Use when you want **all data from the main table**, even if related data is missing.

---
