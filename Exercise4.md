# 🎯 SQL Bolt — Exercise 4 (Sorting & Pagination)

<p align="center">
  📊 Master SQL using <b>DISTINCT, ORDER BY, LIMIT, OFFSET</b>
</p>

--- 

## 📌 Overview

This exercise focuses on **sorting, removing duplicates, and pagination** in SQL.

You will learn how to:

* 🔁 Remove duplicates using `DISTINCT`
* 📊 Sort data using `ORDER BY`
* 🔢 Limit results using `LIMIT`
* ⏭ Skip rows using `OFFSET`

---

## 📊 Table Used: `movies`

| id | title               | director       | year | length_minutes |
| -- | ------------------- | -------------- | ---- | -------------- |
| 1  | Brave               | Brenda Chapman | 2012 | 102            |
| 2  | The Incredibles     | Brad Bird      | 2004 | 116            |
| 3  | Monsters University | Dan Scanlon    | 2013 | 110            |
| 4  | A Bug's Life        | John Lasseter  | 1998 | 95             |
| 5  | Cars 2              | John Lasseter  | 2011 | 120            |
| 6  | Monsters, Inc.      | Pete Docter    | 2001 | 92             |
| 7  | Toy Story 2         | John Lasseter  | 1999 | 93             |
| 8  | WALL-E              | Andrew Stanton | 2008 | 104            |
| 9  | Finding Nemo        | Andrew Stanton | 2003 | 107            |
| 10 | Ratatouille         | Brad Bird      | 2007 | 115            |
| 11 | Up                  | Pete Docter    | 2009 | 101            |
| 12 | Cars                | John Lasseter  | 2006 | 117            |
| 13 | Toy Story           | John Lasseter  | 1995 | 81             |
| 14 | Toy Story 3         | Lee Unkrich    | 2010 | 103            |

---

# 📝 Exercise 4 — Solutions

---

## 🔹 1. List all directors (alphabetically, without duplicates)

```sql
SELECT DISTINCT director
FROM movies
ORDER BY director ASC;
```
<img width="425" height="586" alt="image" src="https://github.com/user-attachments/assets/892f9137-a7bd-4b0a-80c5-92ee35e08f72" />


💡 Removes duplicate names and sorts A → Z

---

## 🔹 2. List the last four Pixar movies (most recent → least)

```sql
SELECT *
FROM movies
ORDER BY year DESC
LIMIT 4;
```
<img width="846" height="624" alt="image" src="https://github.com/user-attachments/assets/08ebd74b-855a-4666-a66d-98225ddee686" />


💡 Shows newest 4 movies first

---

## 🔹 3. List the first five Pixar movies (alphabetically)

```sql
SELECT *
FROM movies
ORDER BY title ASC
LIMIT 5;
```
<img width="815" height="604" alt="image" src="https://github.com/user-attachments/assets/39c08cf3-2e24-427d-81fc-4510bb8d46ad" />


💡 Sorted by title (A → Z)

---

## 🔹 4. List the next five Pixar movies (alphabetically)

```sql
SELECT *
FROM movies
ORDER BY title ASC
LIMIT 5 OFFSET 5;
```
<img width="848" height="606" alt="image" src="https://github.com/user-attachments/assets/2056a560-063b-4f1a-af7a-f4054b19fa66" />


💡 Skips first 5, then shows next 5

---

## ⚙️ Key Concepts Used

| Concept  | Description              |
| -------- | ------------------------ |
| DISTINCT | Removes duplicate values |
| ORDER BY | Sorts results            |
| ASC      | Ascending order (A → Z)  |
| DESC     | Descending order         |
| LIMIT    | Restricts number of rows |
| OFFSET   | Skips rows               |

---

## 🚀 How to Run

1. Open SQLBolt or any SQL tool
2. Copy the queries
3. Execute them
4. Compare results

---

## 🌟 Features

✨ Clean & structured queries
✨ Beginner-friendly explanation
✨ Real dataset practice
✨ GitHub portfolio ready

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

## 💬 Tip

```sql
ORDER BY column ASC   -- ascending
ORDER BY column DESC  -- descending
LIMIT n               -- number of rows
OFFSET n              -- skip rows
```

---

