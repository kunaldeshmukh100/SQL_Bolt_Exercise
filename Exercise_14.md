# 🎯 SQL Bolt — Exercise 14 (UPDATE Queries)

<p align="center">
  ✏️ Learn how to <b>update and correct existing data</b> in SQL tables
</p>

---

## 📌 Overview

In this exercise, we fix incorrect entries in the **Movies** table using the `UPDATE` statement.

This represents a **real-world data cleaning scenario**, where incorrect values must be corrected safely.

---

## 🧠 Concepts Covered

✔ UPDATE statement
✔ SET clause
✔ WHERE condition
✔ Data correction
✔ Safe query practices

---

## 🗂️ Table Used (Before Update)

### 🎬 Movies

| id | title               | director       | year | length_minutes |
| -- | ------------------- | -------------- | ---- | -------------- |
| 1  | Toy Story           | John Lasseter  | 1995 | 81             |
| 2  | A Bug's Life        | El Directore   | 1998 | 95             |
| 3  | Toy Story 2         | John Lasseter  | 1899 | 93             |
| 4  | Monsters, Inc.      | Pete Docter    | 2001 | 92             |
| 5  | Finding Nemo        | Andrew Stanton | 2003 | 107            |
| 6  | The Incredibles     | Brad Bird      | 2004 | 116            |
| 7  | Cars                | John Lasseter  | 2006 | 117            |
| 8  | Ratatouille         | Brad Bird      | 2007 | 115            |
| 9  | WALL-E              | Andrew Stanton | 2008 | 104            |
| 10 | Up                  | Pete Docter    | 2009 | 101            |
| 11 | Toy Story 8         | El Directore   | 2010 | 103            |
| 12 | Cars 2              | John Lasseter  | 2011 | 120            |
| 13 | Brave               | Brenda Chapman | 2012 | 102            |
| 14 | Monsters University | Dan Scanlon    | 2013 | 110            |

---

# 📝 Exercise 14 — Tasks

1. Fix director of **A Bug's Life**
2. Correct release year of **Toy Story 2**
3. Fix title and director of incorrect movie (**Toy Story 8**)

---

# ✅ Solutions

---

## 🔹 1. Correct Director

```sql
UPDATE movies
SET director = 'John Lasseter'
WHERE id = 2;
```
<img width="856" height="585" alt="image" src="https://github.com/user-attachments/assets/7f254e40-ded5-4647-9922-4b1e901e6a8d" />



---

## 🔹 2. Correct Year

```sql
UPDATE movies
SET year = 1999
WHERE id = 3;
```
<img width="881" height="576" alt="image" src="https://github.com/user-attachments/assets/4dfe37b0-d110-47d3-97b2-6988c5942c56" />

---

## 🔹 3. Correct Title & Director

```sql
UPDATE movies
SET title = 'Toy Story 3',
    director = 'Lee Unkrich'
WHERE id = 11;
```
<img width="736" height="607" alt="image" src="https://github.com/user-attachments/assets/c31067b2-cfda-4c63-a75b-0372ce84d7c8" />


---

# 🎬 Table After Update (Corrected Data)

| id | title               | director       | year | length_minutes |
| -- | ------------------- | -------------- | ---- | -------------- |
| 1  | Toy Story           | John Lasseter  | 1995 | 81             |
| 2  | A Bug's Life        | John Lasseter  | 1998 | 95             |
| 3  | Toy Story 2         | John Lasseter  | 1999 | 93             |
| 4  | Monsters, Inc.      | Pete Docter    | 2001 | 92             |
| 5  | Finding Nemo        | Andrew Stanton | 2003 | 107            |
| 6  | The Incredibles     | Brad Bird      | 2004 | 116            |
| 7  | Cars                | John Lasseter  | 2006 | 117            |
| 8  | Ratatouille         | Brad Bird      | 2007 | 115            |
| 9  | WALL-E              | Andrew Stanton | 2008 | 104            |
| 10 | Up                  | Pete Docter    | 2009 | 101            |
| 11 | Toy Story 3         | Lee Unkrich    | 2010 | 103            |
| 12 | Cars 2              | John Lasseter  | 2011 | 120            |
| 13 | Brave               | Brenda Chapman | 2012 | 102            |
| 14 | Monsters University | Dan Scanlon    | 2013 | 110            |

---

## ⚙️ Syntax Used

```sql
UPDATE table_name
SET column = value
WHERE condition;
```

---

## ⚠️ Important Notes

🚨 Always use a `WHERE` clause
Without it, ALL rows will be updated!

❌ Dangerous:

```sql
UPDATE movies SET director = 'John Lasseter';
```

---

## 🚀 How to Run

1. Open SQLBolt / MySQL / SQLite
2. Run the UPDATE queries
3. Verify results:

```sql
SELECT * FROM movies;
```

---

## 🌟 Features

✨ Real-world data correction
✨ Beginner-friendly SQL
✨ Clean and structured queries
✨ GitHub portfolio ready

---

## 👨‍💻 Author

**Kunal Deshmukh**

---

## ⭐ Support

If you found this helpful:

⭐ Star the repository
🔁 Share with others
🚀 Keep learning SQL

---

## 💬 Pro Tip

👉 Always test before updating:

```sql
SELECT * FROM movies WHERE id = 2;
```

✔ Ensures safe and accurate updates

---
