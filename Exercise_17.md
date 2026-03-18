# 🎯 SQL Bolt — Exercise 17 (ALTER TABLE)

<p align="center">
  🛠️ Learn how to <b>modify existing tables</b> in SQL
</p>

---

## 📌 Overview

In this exercise, we update the **structure of an existing table** by adding new columns.

This is useful when:

* 📊 Requirements change
* 🆕 New data needs to be stored
* 🛠️ Database evolves over time

---

## 🧠 Concepts Covered

✔ ALTER TABLE
✔ Adding new columns
✔ Default values
✔ Schema modification

---

## 🗂️ Table Used

## 🎬 Movies Table (Before ALTER TABLE)

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


---

## 📌 Notes

* **Aspect_ratio** → Currently `NULL` (no values inserted yet)
* **Language** → Default value applied → `English`
* Existing rows automatically received default values

---


---

# 📝 Exercise 17 — Tasks

1. Add a column **Aspect_ratio** (FLOAT)
2. Add a column **Language** (TEXT) with default = **'English'**

---

# ✅ Solutions

---

## 🔹 1. Add Aspect Ratio Column

```sql
ALTER TABLE movies
ADD Aspect_ratio FLOAT;
```
<img width="920" height="575" alt="image" src="https://github.com/user-attachments/assets/ba1a11d2-5895-413c-a9af-a8aed75813a8" />

---

## 🔹 2. Add Language Column with Default

```sql
ALTER TABLE movies
ADD Language TEXT DEFAULT 'English';
```
<img width="909" height="614" alt="image" src="https://github.com/user-attachments/assets/b9fef261-d9f5-4961-b76c-8ae4c5fe832f" />

---

## 🎬 Movies Table (After ALTER TABLE)

| id | title               | director       | year | length_minutes | Aspect_ratio | Language |
| -- | ------------------- | -------------- | ---- | -------------- | ------------ | -------- |
| 1  | Toy Story           | John Lasseter  | 1995 | 81             | NULL         | English  |
| 2  | A Bug's Life        | John Lasseter  | 1998 | 95             | NULL         | English  |
| 3  | Toy Story 2         | John Lasseter  | 1999 | 93             | NULL         | English  |
| 4  | Monsters, Inc.      | Pete Docter    | 2001 | 92             | NULL         | English  |
| 5  | Finding Nemo        | Andrew Stanton | 2003 | 107            | NULL         | English  |
| 6  | The Incredibles     | Brad Bird      | 2004 | 116            | NULL         | English  |
| 7  | Cars                | John Lasseter  | 2006 | 117            | NULL         | English  |
| 8  | Ratatouille         | Brad Bird      | 2007 | 115            | NULL         | English  |
| 9  | WALL-E              | Andrew Stanton | 2008 | 104            | NULL         | English  |
| 10 | Up                  | Pete Docter    | 2009 | 101            | NULL         | English  |
| 11 | Toy Story 3         | Lee Unkrich    | 2010 | 103            | NULL         | English  |
| 12 | Cars 2              | John Lasseter  | 2011 | 120            | NULL         | English  |
| 13 | Brave               | Brenda Chapman | 2012 | 102            | NULL         | English  |
| 14 | Monsters University | Dan Scanlon    | 2013 | 110            | NULL         | English  |

---

## 📌 Notes

* **Aspect_ratio** → Currently `NULL` (no values inserted yet)
* **Language** → Default value applied → `English`
* Existing rows automatically received default values

---


---

## ⚙️ Syntax Used

```sql
ALTER TABLE table_name
ADD column_name datatype DEFAULT value;
```

---

## 📊 Explanation

* **FLOAT** → stores decimal values (aspect ratio like 1.85, 2.35)
* **TEXT** → stores string values (language)
* **DEFAULT 'English'** → assigns value automatically

---

## ⚠️ Important Notes

🚨 Existing rows:

* New column values → `NULL` (unless default is set)

---

## 🚀 How to Run

1. Open SQLBolt / MySQL / SQLite
2. Run ALTER TABLE queries
3. Verify using:

```sql
SELECT * FROM movies;
```

---

## 🌟 Features

✨ Schema modification
✨ Real-world database evolution
✨ Beginner-friendly
✨ GitHub portfolio ready

---

## 👨‍💻 Author

**Kunal Deshmukh**

---

## ⭐ Support

If this helped:

⭐ Star the repository
🚀 Share with others
📘 Keep learning SQL

---

## 💬 Pro Tip

👉 Always check structure:

```sql
PRAGMA table_info(movies);
```

✔ Shows all columns in SQLite

---
