# 🎯 SQL Bolt — Exercise 10 (Aggregation Functions)

<p align="center">
  📊 Learn SQL aggregation using <b>MAX, AVG, SUM, GROUP BY</b>
</p>

--- 

## 📌 Overview

This exercise focuses on **aggregation functions**, used to analyze grouped data.

You will learn how to:

* 🔝 Find maximum values
* 📊 Calculate averages
* ➕ Sum values
* 🧠 Group data using `GROUP BY`

---

## 🧠 Concepts Used

```sql
MAX(column)
AVG(column)
SUM(column)
GROUP BY column
```

💡 Aggregations help summarize data

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

# 📝 Exercise 10 — Solutions

---

## 🔹 1. Longest time worked

```sql
SELECT MAX(years_employed)
FROM employees;
```
<img width="399" height="567" alt="image" src="https://github.com/user-attachments/assets/893d6f06-483e-4da8-ab16-7d486873ca83" />


---

## 🔹 2. Average years per role

```sql
SELECT role, AVG(years_employed)
FROM employees
GROUP BY role;
```
<img width="526" height="573" alt="image" src="https://github.com/user-attachments/assets/433b8ee1-47eb-4643-bdcb-87443563e012" />


---

## 🔹 3. Total years per building

```sql
SELECT building, SUM(years_employed)
FROM employees
GROUP BY building;
```
<img width="537" height="590" alt="image" src="https://github.com/user-attachments/assets/2cb607c8-b885-4f89-8c6a-6a8043c4366a" />


---

## ⚙️ Key Concepts Used

| Concept  | Description   |
| -------- | ------------- |
| MAX      | Highest value |
| AVG      | Average value |
| SUM      | Total sum     |
| GROUP BY | Groups rows   |

---

## 🚀 How to Run

```bash
1. Open SQLBolt or any SQL tool
2. Copy queries
3. Execute them
4. Analyze results
```

---

## 🌟 Features

✨ Data aggregation
✨ Real-world analysis
✨ GROUP BY usage
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
GROUP BY column
```

👉 Always use when combining aggregation with columns

---
