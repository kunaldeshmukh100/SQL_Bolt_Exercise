# 🎯 SQL Bolt — Exercise 11 (COUNT & GROUP BY)

<p align="center">
  📊 Learn SQL aggregation using <b>COUNT, SUM, GROUP BY</b>
</p>

--- 

## 📌 Overview

This exercise focuses on **counting and grouping data** in SQL.

You will learn how to:

* 🔢 Count rows using `COUNT()`
* 📊 Group data using `GROUP BY`
* ➕ Sum values using `SUM()`
* 🎯 Filter specific data using `WHERE`

---

## 🧠 Concepts Used

```sql
COUNT(*)
SUM(column)
GROUP BY column
```

💡 Used for data analysis and reporting

---

## 📊 Table Used: `employees`

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
| Artist   | Brandon J. | 2w       | 7              |

---

# 📝 Exercise 11 — Solutions

---

## 🔹 1. Number of Artists

```sql
SELECT COUNT(*)
FROM employees
WHERE role = 'Artist';
```
<img width="412" height="613" alt="image" src="https://github.com/user-attachments/assets/713faae1-68dc-43e0-9d7e-50a58d0e305e" />



---

## 🔹 2. Employees per role

```sql
SELECT role, COUNT(*)
FROM employees
GROUP BY role;
```
<img width="570" height="580" alt="image" src="https://github.com/user-attachments/assets/633534c2-c6fc-42ca-bcfb-9a0edb6773fe" />

---

## 🔹 3. Total years of Engineers

```sql
SELECT SUM(years_employed)
FROM employees
WHERE role = 'Engineer';
```
<img width="434" height="584" alt="image" src="https://github.com/user-attachments/assets/a0b1cda6-ce5a-493a-ab38-9fff3b80c520" />


---

## ⚙️ Key Concepts Used

| Concept  | Description  |
| -------- | ------------ |
| COUNT    | Counts rows  |
| SUM      | Adds values  |
| GROUP BY | Groups rows  |
| WHERE    | Filters rows |

---

## 🚀 How to Run

```bash
1. Open SQLBolt or any SQL tool
2. Copy the queries
3. Execute them
4. Analyze results
```

---

## 🌟 Features

✨ Data counting
✨ Group analysis
✨ Real-world reporting
✨ Beginner-friendly

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
COUNT(*)
```

👉 Counts all rows including duplicates

---
