# SQL_Bolt_Exercise
This repository contains structured SQL exercises and examples designed to help beginners understand database querying, including SELECT statements, filtering, and data retrieval techniques.

# 🚀 SQL Bolt Complete Exercises (1–18) — Master SQL from Beginner to Advanced

<p align="center">
  📊 A complete hands-on SQL learning journey using SQLBolt  
  From basics → joins → aggregation → database design → cleanup
</p>

---

# 📌 About This Repository

This repository contains **all SQLBolt exercises (1–18)** with:

* ✅ Queries
* ✅ Explanations
* ✅ Concepts
* ✅ Real-world understanding

Perfect for:

* 🧑‍🎓 Students
* 💻 Beginners
* 🎯 Interview preparation

---

# 🧠 Concepts Covered (Complete Roadmap)

✔ SELECT
✔ WHERE
✔ ORDER BY
✔ LIMIT
✔ LIKE
✔ JOIN (INNER, LEFT)
✔ NULL handling
✔ GROUP BY & Aggregation
✔ INSERT
✔ UPDATE
✔ DELETE
✔ CREATE TABLE
✔ ALTER TABLE
✔ DROP TABLE

---

# 📝 Exercise-wise Breakdown

---

# 🔹 Exercise 1 — Basic SELECT

### 🎯 Goal:

Retrieve data from table

```sql
SELECT title FROM movies;
SELECT director FROM movies;
SELECT title, director FROM movies;
SELECT title, year FROM movies;
SELECT * FROM movies;
```

💡 **Concept:**

* SELECT retrieves columns
* `*` = all columns

---

# 🔹 Exercise 2 — Filtering with WHERE

```sql
SELECT * FROM movies WHERE id = 6;

SELECT * FROM movies
WHERE year BETWEEN 2000 AND 2010;

SELECT * FROM movies
WHERE year NOT BETWEEN 2000 AND 2010;

SELECT title, year FROM movies
ORDER BY year LIMIT 5;
```

💡 **Concept:**

* WHERE filters rows
* BETWEEN for ranges

---

# 🔹 Exercise 3 — Pattern Matching

```sql
SELECT * FROM movies WHERE title LIKE 'Toy Story%';

SELECT * FROM movies WHERE director = 'John Lasseter';

SELECT title, director FROM movies
WHERE director != 'John Lasseter';

SELECT * FROM movies WHERE title LIKE 'WALL-%';
```

💡 **Concept:**

* LIKE = pattern matching
* `%` wildcard

---

# 🔹 Exercise 4 — DISTINCT & ORDER

```sql
SELECT DISTINCT director FROM movies ORDER BY director;

SELECT * FROM movies ORDER BY year DESC LIMIT 4;

SELECT * FROM movies ORDER BY title LIMIT 5;

SELECT * FROM movies ORDER BY title LIMIT 5 OFFSET 5;
```

💡 **Concept:**

* DISTINCT removes duplicates
* OFFSET skips rows

---

# 🔹 Exercise 5 — Sorting & Limits

```sql
SELECT city, population FROM north_american_cities
WHERE country = 'Canada';

SELECT * FROM north_american_cities
WHERE country = 'United States'
ORDER BY latitude DESC;

SELECT * FROM north_american_cities
WHERE longitude < -87.629798
ORDER BY longitude;

SELECT * FROM north_american_cities
WHERE country = 'Mexico'
ORDER BY population DESC LIMIT 2;

SELECT * FROM north_american_cities
WHERE country = 'United States'
ORDER BY population DESC LIMIT 2 OFFSET 2;
```

---

# 🔹 Exercise 6 — INNER JOIN

```sql
SELECT title, domestic_sales, international_sales
FROM movies
JOIN boxoffice
ON movies.id = boxoffice.movie_id;

SELECT title
FROM movies
JOIN boxoffice
ON movies.id = boxoffice.movie_id
WHERE international_sales > domestic_sales;

SELECT title, rating
FROM movies
JOIN boxoffice
ON movies.id = boxoffice.movie_id
ORDER BY rating DESC;
```

💡 **Concept:**

* JOIN combines tables

---

# 🔹 Exercise 7 — LEFT JOIN

```sql
SELECT DISTINCT building FROM employees;

SELECT building_name, capacity FROM buildings;

SELECT buildings.building_name, employees.role
FROM buildings
LEFT JOIN employees
ON buildings.building_name = employees.building;
```

💡 **Concept:**

* LEFT JOIN includes all rows

---

# 🔹 Exercise 8 — NULL Handling

```sql
SELECT name, role FROM employees
WHERE building IS NULL;

SELECT building_name FROM buildings
LEFT JOIN employees
ON buildings.building_name = employees.building
WHERE employees.name IS NULL;
```

💡 **Concept:**

* NULL means missing data

---

# 🔹 Exercise 9 — Calculations

```sql
SELECT title,
(domestic_sales + international_sales) / 1000000 AS total_sales
FROM movies
JOIN boxoffice
ON movies.id = boxoffice.movie_id;

SELECT title, rating * 10 AS rating_percent
FROM movies
JOIN boxoffice
ON movies.id = boxoffice.movie_id;

SELECT * FROM movies WHERE year % 2 = 0;
```

---

# 🔹 Exercise 10 — Aggregation Basics

```sql
SELECT MAX(years_employed) FROM employees;

SELECT role, AVG(years_employed)
FROM employees GROUP BY role;

SELECT building, SUM(years_employed)
FROM employees GROUP BY building;
```

---

# 🔹 Exercise 11 — COUNT

```sql
SELECT COUNT(*) FROM employees WHERE role = 'Artist';

SELECT role, COUNT(*) FROM employees GROUP BY role;

SELECT SUM(years_employed)
FROM employees WHERE role = 'Engineer';
```

---

# 🔹 Exercise 12 — GROUP BY + JOIN

```sql
SELECT director, COUNT(*) FROM movies GROUP BY director;

SELECT director,
SUM(domestic_sales),
SUM(international_sales)
FROM movies
JOIN boxoffice
ON movies.id = boxoffice.movie_id
GROUP BY director;
```

---

# 🔹 Exercise 13 — INSERT

```sql
INSERT INTO movies VALUES (15, 'Toy Story 4', 'John Lasseter', 2019, 100);

INSERT INTO boxoffice VALUES (15, 8.7, 340000000, 270000000);
```

---

# 🔹 Exercise 14 — UPDATE

```sql
UPDATE movies SET director = 'John Lasseter' WHERE id = 2;

UPDATE movies SET year = 1999 WHERE id = 3;

UPDATE movies
SET title = 'Toy Story 3', director = 'Lee Unkrich'
WHERE id = 11;
```

---

# 🔹 Exercise 15 — DELETE

```sql
DELETE FROM movies WHERE year < 2005;

DELETE FROM movies WHERE director = 'Andrew Stanton';
```

---

# 🔹 Exercise 16 — CREATE TABLE

```sql
CREATE TABLE Database (
Name TEXT,
Version FLOAT,
Download_count INTEGER
);
```

---

# 🔹 Exercise 17 — ALTER TABLE

```sql
ALTER TABLE movies ADD Aspect_ratio FLOAT;

ALTER TABLE movies ADD Language TEXT DEFAULT 'English';
```

---

# 🔹 Exercise 18 — DROP TABLE

```sql
DROP TABLE IF EXISTS movies;
DROP TABLE IF EXISTS boxoffice;
```

---

# 🎯 Final Summary

| Category          | Skills Learned         |
| ----------------- | ---------------------- |
| Basic Queries     | SELECT, WHERE          |
| Filtering         | LIKE, BETWEEN          |
| Sorting           | ORDER BY, LIMIT        |
| Joins             | INNER, LEFT            |
| Data Handling     | NULL                   |
| Aggregation       | COUNT, SUM, AVG        |
| Data Manipulation | INSERT, UPDATE, DELETE |
| Database Design   | CREATE, ALTER          |
| Cleanup           | DROP TABLE             |

---

# 🚀 Final Outcome

After completing all exercises, you can:

✅ Query real datasets
✅ Join multiple tables
✅ Perform analytics
✅ Modify database
✅ Design schemas
✅ Handle production-level SQL

---

# 👨‍💻 Author

**Kunal Deshmukh**

---

# ⭐ Support

If you found this useful:

⭐ Star the repository
🔁 Share with others
🚀 Keep building projects

---

# 🔥 Next Level

👉 Build **real-world SQL project**
👉 Learn **Indexes + Optimization + Normalization**
👉 Practice **LeetCode SQL problems**

---
