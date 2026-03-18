# 🎯 SQL Bolt — Exercise 2 (Filtering Queries)

<p align="center">
  🚀 Learn SQL filtering using <b>WHERE, BETWEEN, NOT, ORDER BY, LIMIT</b>
</p>

--- 

## 📌 Overview

This exercise focuses on **filtering data** from a database using SQL conditions.

You will learn how to:

* 🔍 Filter rows using `WHERE`
* 📅 Work with ranges using `BETWEEN`
* ❌ Exclude data using `NOT`
* 📊 Sort data using `ORDER BY`
* 🔢 Limit results using `LIMIT`

---

## 📊 Table Used: `movies`

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

# 📝 Exercise 2 — Solutions

---

## 🔹 1. Find the movie with a row id of 6

```sql
SELECT * 
FROM movies
WHERE id = 6;
```
<img width="782" height="581" alt="image" src="https://github.com/user-attachments/assets/75f47194-b541-491b-a891-604327720c5c" />


---

## 🔹 2. Find movies released between 2000 and 2010

```sql
SELECT * 
FROM movies
WHERE year BETWEEN 2000 AND 2010;
```
<img width="823" height="589" alt="image" src="https://github.com/user-attachments/assets/3aead27c-e53f-4960-b779-084e5df87419" />


---

## 🔹 3. Find movies NOT released between 2000 and 2010

```sql
SELECT * 
FROM movies
WHERE year NOT BETWEEN 2000 AND 2010;
```
<img width="853" height="601" alt="image" src="https://github.com/user-attachments/assets/536696ae-0cde-431d-8af2-ba8436d28b65" />


---

## 🔹 4. Find the first 5 Pixar movies and their release year

```sql
SELECT title, year
FROM movies
ORDER BY year
LIMIT 5;
```
<img width="785" height="631" alt="image" src="https://github.com/user-attachments/assets/82dcae58-827b-4a93-9584-df4e31758ae3" />


---

## ⚙️ Key Concepts Used

| Concept  | Description                     |
| -------- | ------------------------------- |
| WHERE    | Filters rows based on condition |
| BETWEEN  | Selects range of values         |
| NOT      | Excludes values                 |
| ORDER BY | Sorts results                   |
| LIMIT    | Restricts number of rows        |

---

## 🚀 How to Run

1. Open SQLBolt or any SQL tool
2. Copy the queries
3. Execute them
4. Compare results

---

## 👨‍💻 Author

**Kunal Deshmukh**

---

## ⭐ Support

If you found this helpful:

* ⭐ Star the repo
* 🔁 Share with others
* 🚀 Keep learning SQL

---

