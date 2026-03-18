# 🎯 SQL Bolt — Exercise 9 (Calculations & Expressions)

<p align="center">
  📊 Learn SQL calculations using <b>JOIN + Arithmetic + Expressions</b>
</p>

--- 

## 📌 Overview

This exercise focuses on performing **calculations inside SQL queries**.

You will learn how to:

* ➕ Combine columns using arithmetic
* 💰 Convert values into readable formats
* 📊 Transform ratings into percentages
* 🔢 Filter data using mathematical conditions

---

## 🧠 Concepts Used

```sql
SELECT column1 + column2
SELECT column * value
WHERE column % 2 = 0
```

💡 SQL can perform calculations directly inside queries

---

## 📊 Tables Used

### 🎬 Movies

* id
* title
* year

### 💰 BoxOffice

* movie_id
* domestic_sales
* international_sales
* rating

---

# 📝 Exercise 9 — Solutions

---

## 🔹 1. Movies with combined sales (in millions)

```sql
SELECT movies.title,
       (boxoffice.domestic_sales + boxoffice.international_sales) / 1000000 AS total_sales_millions
FROM movies
JOIN boxoffice
ON movies.id = boxoffice.movie_id;
```
<img width="938" height="698" alt="image" src="https://github.com/user-attachments/assets/d1bda43d-0af6-49c6-8d96-4fc5b84c2d7c" />


---

## 🔹 2. Movies with ratings in percent

```sql
SELECT movies.title,
       boxoffice.rating * 10 AS rating_percent
FROM movies
JOIN boxoffice
ON movies.id = boxoffice.movie_id;
```
<img width="771" height="640" alt="image" src="https://github.com/user-attachments/assets/fa5e558e-e078-48e3-b8e9-ac2af35ecb4f" />


---

## 🔹 3. Movies released in even-numbered years

```sql
SELECT *
FROM movies
WHERE year % 2 = 0;
```
<img width="834" height="604" alt="image" src="https://github.com/user-attachments/assets/cad36208-9ec7-4f97-b2ef-af532416d7d2" />


---

## ⚙️ Key Concepts Used

| Concept | Description         |
| ------- | ------------------- |
| +       | Addition            |
| *       | Multiplication      |
| /       | Division            |
| %       | Modulus (remainder) |
| JOIN    | Combine tables      |
| AS      | Rename column       |

---

## 🚀 How to Run

```bash
1. Open SQLBolt or any SQL tool
2. Copy the queries
3. Execute them
4. Observe calculated results
```

---

## 🌟 Features

✨ Arithmetic in SQL
✨ Real-world data calculations
✨ JOIN + expressions
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
AS column_name
```

👉 Use to rename calculated columns for clean output

---
