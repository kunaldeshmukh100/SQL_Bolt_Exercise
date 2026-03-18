# 🎯 SQL Bolt — Exercise 7 (OUTER JOINs)

<p align="center">
  🏢 Learn how to use <b>LEFT JOIN</b> to include missing data
</p>

--- 

## 📌 Overview

This exercise introduces **OUTER JOINs**, specifically the `LEFT JOIN`.

You will learn how to:

* 🔗 Combine data from multiple tables
* 🏢 Include all records from one table
* ⚠️ Handle `NULL` values (missing data)
* 👨‍💼 Analyze employee roles per building

---

## 🧠 Concept: LEFT JOIN

```sql
SELECT column1, column2
FROM table1
LEFT JOIN table2
ON table1.key = table2.key;
```

💡

* Keeps **all rows from the left table**
* If no match → shows `NULL`

---

## 📊 Tables Used

### 🏢 Buildings Table

| building_name | capacity |
| ------------- | -------- |
| 1e            | 24       |
| 1w            | 32       |
| 2e            | 16       |
| 2w            | 20       |

---

### 👨‍💼 Employees Table

| role     | name       | building | years_employed |
| -------- | ---------- | -------- | -------------- |
| Engineer | Becky A.   | 1e       | 4              |
| Engineer | Dan B.     | 1e       | 2              |
| Engineer | Sharon F.  | 1e       | 6              |
| Engineer | Dan M.     | 1e       | 4              |
| Engineer | Malcom S.  | 1e       | 1              |
| Artist   | Tylar S.   | 2w       | 2              |
| Artist   | Sherman D. | 2w       | 8              |
| Artist   | Jakob J.   | 2w       | 6              |
| Artist   | Lillia A.  | 2w       | 7              |

---

# 📝 Exercise 7 — Solutions

---

## 🔹 1. Find all buildings that have employees

```sql
SELECT DISTINCT building
FROM employees;
```
<img width="389" height="566" alt="image" src="https://github.com/user-attachments/assets/37aef546-26bc-497d-b11b-ae807c955276" />


💡 Uses `employees.building`

---

## 🔹 2. List all buildings and their capacity

```sql
SELECT building_name, capacity
FROM buildings;
```
<img width="710" height="554" alt="image" src="https://github.com/user-attachments/assets/9ad734b5-aa98-462b-b015-da31eb4b8fe3" />


💡 Includes empty buildings too

---

## 🔹 3. List all buildings and distinct employee roles (including empty buildings)

```sql
SELECT DISTINCT buildings.building_name, employees.role
FROM buildings
LEFT JOIN employees
ON buildings.building_name = employees.building
ORDER BY buildings.building_name;
```
<img width="765" height="626" alt="image" src="https://github.com/user-attachments/assets/a4c20d36-5f8c-44a3-98fe-567fe76a208b" />


💡

* Keeps all buildings
* Shows roles if exist
* Shows `NULL` if no employees

---

## ⚙️ Key Concepts Used

| Concept   | Description                       |
| --------- | --------------------------------- |
| LEFT JOIN | Includes all rows from left table |
| DISTINCT  | Removes duplicates                |
| NULL      | Missing value                     |
| ON        | Join condition                    |
| ORDER BY  | Sorting                           |

---

## 🚀 How to Run

```bash
1. Open SQLBolt or any SQL tool
2. Copy the queries
3. Execute them
4. Observe NULL values for empty buildings
```

---

## 🌟 Features

✨ Outer join practice
✨ Real-world scenario (empty buildings)
✨ Beginner-friendly explanation
✨ Portfolio-ready SQL

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
