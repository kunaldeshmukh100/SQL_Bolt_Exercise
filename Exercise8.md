# 🎯 SQL Bolt — Exercise 8 (NULL Handling)

<p align="center">
  ⚠️ Learn how to work with <b>NULL values</b> in SQL using <b>IS NULL</b> and <b>LEFT JOIN</b>
</p>

--- 

## 📌 Overview

This exercise focuses on handling **NULL values**, which represent **missing or unknown data**.

You will learn how to:

* ❓ Identify missing values using `IS NULL`
* ❌ Filter non-missing values using `IS NOT NULL`
* 🔗 Combine tables using `LEFT JOIN`
* 🏢 Detect employees without buildings and empty buildings

---

## 🧠 Concept: NULL in SQL

```sql
SELECT column
FROM table
WHERE column IS NULL;
```

💡

* `NULL` ≠ 0 or empty string
* Use `IS NULL` or `IS NOT NULL` (not `=`)

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
| Artist   | Unknown    | NULL     | 0              |

---

# 📝 Exercise 8 — Solutions

---

## 🔹 1. Find employees without a building

```sql id="6w9gcl"
SELECT name, role
FROM employees
WHERE building IS NULL;
```
<img width="608" height="604" alt="image" src="https://github.com/user-attachments/assets/d39b9aa9-c2cd-439d-a265-83b1e7d3bc7a" />


💡 Finds employees who are **not assigned to any building**

---

## 🔹 2. Find buildings that have no employees

```sql id="lyy6pb"
SELECT buildings.building_name
FROM buildings
LEFT JOIN employees
ON buildings.building_name = employees.building
WHERE employees.building IS NULL;
```
<img width="780" height="634" alt="image" src="https://github.com/user-attachments/assets/eafc8cdd-2ef6-4d85-a734-cfdadd3c8eef" />


💡

* Uses `LEFT JOIN` to include all buildings
* Filters where no employee exists → `NULL`

---

## ⚙️ Key Concepts Used

| Concept     | Description                    |
| ----------- | ------------------------------ |
| NULL        | Missing/unknown value          |
| IS NULL     | Checks for NULL                |
| IS NOT NULL | Checks non-NULL                |
| LEFT JOIN   | Keeps all rows from left table |
| WHERE       | Filters data                   |

---

## 🚀 How to Run

```bash id="y5dh8v"
1. Open SQLBolt or any SQL tool
2. Copy the queries
3. Execute them
4. Observe NULL behavior
```

---

## 🌟 Features

✨ NULL handling practice
✨ Real-world missing data scenario
✨ JOIN + filtering combination
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

```sql id="qf78yt"
WHERE column IS NULL
WHERE column IS NOT NULL
```

👉 Never use:

```sql id="h7h8sm"
WHERE column = NULL   -- ❌ Wrong
```

---
