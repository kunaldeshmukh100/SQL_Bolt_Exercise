# 🎯 SQL Bolt — Exercise 15 (DELETE Queries)

<p align="center">
  🗑️ Learn how to remove unwanted data from SQL tables
</p>

---

## 📌 Overview

This exercise focuses on:

* 🗑️ Deleting records from a table
* 🎯 Filtering rows using conditions
* ⚠️ Understanding safe deletion practices

---

## 🧠 Concepts Covered

✔ DELETE statement
✔ WHERE condition
✔ Data filtering
✔ Safe deletion

---

## 🗂️ Table Used (Before Deletion)

### 🎬 Movies (Sample)

| id | title           | director       | year |
| -- | --------------- | -------------- | ---- |
| 1  | Toy Story       | John Lasseter  | 1995 |
| 2  | A Bug's Life    | John Lasseter  | 1998 |
| 3  | Toy Story 2     | John Lasseter  | 1999 |
| 4  | Monsters, Inc.  | Pete Docter    | 2001 |
| 5  | Finding Nemo    | Andrew Stanton | 2003 |
| 6  | The Incredibles | Brad Bird      | 2004 |
| 7  | Cars            | John Lasseter  | 2006 |
| 8  | Ratatouille     | Brad Bird      | 2007 |
| 9  | WALL-E          | Andrew Stanton | 2008 |
| 10 | Up              | Pete Docter    | 2009 |

---

# 📝 Exercise 15 — Tasks

1. Remove all movies released before 2005
2. Remove all movies directed by Andrew Stanton

---

# ✅ Solutions

---

## 🔹 1. Delete old movies

```sql
DELETE FROM movies
WHERE year < 2005;
```
<img width="840" height="560" alt="image" src="https://github.com/user-attachments/assets/13aae17d-ff20-4f9c-9123-bb33fe9fd28c" />

---

## 🔹 2. Delete movies by Andrew Stanton

```sql
DELETE FROM movies
WHERE director = 'Andrew Stanton';
```
<img width="852" height="575" alt="image" src="https://github.com/user-attachments/assets/22ac0f47-c3d8-4ad4-901e-2dcfd445013f" />

---

# 🎬 Table After Deletion

| id | title       | director      | year |
| -- | ----------- | ------------- | ---- |
| 7  | Cars        | John Lasseter | 2006 |
| 8  | Ratatouille | Brad Bird     | 2007 |
| 10 | Up          | Pete Docter   | 2009 |

---

## ⚙️ Syntax Used

```sql
DELETE FROM table_name
WHERE condition;
```

---

## ⚠️ Important Notes

🚨 Always use WHERE clause

❌ Dangerous:

```sql
DELETE FROM movies;
```

👉 Deletes ALL data

---

## 🚀 How to Run

1. Open SQLBolt / MySQL / SQLite
2. Run DELETE queries
3. Verify results:

```sql
SELECT * FROM movies;
```

---

## 🌟 Features

✨ Data cleanup queries
✨ Real-world scenarios
✨ Beginner-friendly
✨ GitHub portfolio ready

---

## 👨‍💻 Author

**Kunal Deshmukh**

---

## ⭐ Support

If you liked this:

⭐ Star the repo
🚀 Share with friends
📘 Keep practicing SQL

---

## 💬 Pro Tip

👉 Always test before deleting:

```sql
SELECT * FROM movies WHERE year < 2005;
```

✔ Prevents accidental data loss

---
