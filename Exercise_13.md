# 🎯 SQL Bolt — Exercise 13 (INSERT Queries)

<p align="center">
  ➕ Learn how to insert new records into database tables
</p>

--- 

## 📌 Overview

This exercise focuses on:

* ➕ INSERT queries
* 🧩 Adding new rows to tables
* 🔗 Maintaining relationships between tables

---

## 🧠 Concepts Used

```sql
INSERT INTO table_name (column1, column2, ...)
VALUES (value1, value2, ...);
```

---

## 📊 Tables Used

### 🎬 Movies

* id
* title
* director
* year
* length_minutes

### 💰 BoxOffice

* movie_id
* rating
* domestic_sales
* international_sales

---

# 📝 Exercise 13 — Solutions

---

## 🔹 1. Add Toy Story 4 to Movies

```sql
INSERT INTO movies (id, title, director, year, length_minutes)
VALUES (15, 'Toy Story 4', 'John Lasseter', 2019, 100);
```
<img width="864" height="575" alt="image" src="https://github.com/user-attachments/assets/15203257-8fae-408f-883d-1dd9e9fd8bf1" />


---

## 🔹 2. Add BoxOffice Data

```sql
INSERT INTO boxoffice VALUES (4, 8.7, 340000000, 270000000);
```
<img width="873" height="578" alt="image" src="https://github.com/user-attachments/assets/41e9854c-189b-4836-8c52-27739f0ca430" />


---

## ⚙️ Key Concepts

| Concept     | Description       |
| ----------- | ----------------- |
| INSERT INTO | Adds new row      |
| VALUES      | Data to insert    |
| Primary Key | Unique identifier |
| Foreign Key | Connects tables   |

---

## 🚀 How to Run

```bash
1. Open SQLBolt / MySQL / SQLite
2. Run INSERT queries
3. Verify using SELECT *
```

---

## 🌟 Features

✨ Real-world data insertion
✨ Multi-table relationship
✨ Beginner-friendly SQL
✨ GitHub portfolio ready

---

## 👨‍💻 Author

**Kunal Deshmukh**

---

## ⭐ Support

If you like this:
⭐ Star the repo
🚀 Share with friends
💡 Keep practicing SQL

---

## 💬 Pro Tip

Always ensure:

```sql
movie_id = id
```

👉 To maintain correct relationships between tables

---
