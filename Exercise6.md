# 🎯 SQL Bolt — Exercise 6 (JOIN Queries)

<p align="center">
  🔗 Learn how to combine tables using <b>INNER JOIN</b>
</p>

--- 

## 📌 Overview

This exercise introduces **multi-table queries using JOINs**.

You will learn:

* 🔗 How to combine data from multiple tables
* 🎯 Use `INNER JOIN` with keys
* 📊 Compare values across tables
* ⭐ Sort results using joined data

---

## 🧠 Concept: INNER JOIN

```sql
SELECT column1, column2
FROM table1
INNER JOIN table2
ON table1.id = table2.id;
```

💡 Combines rows where keys match in both tables

---

## 📊 Tables Used

### 🎬 Movies Table

* id
* title

### 💰 BoxOffice Table

* movie_id
* domestic_sales
* international_sales
* rating

---

# 📝 Exercise 6 — Solutions

---

## 🔹 1. Domestic & International Sales

```sql
SELECT movies.title, boxoffice.domestic_sales, boxoffice.international_sales
FROM movies
INNER JOIN boxoffice
ON movies.id = boxoffice.movie_id;
```
<img width="930" height="635" alt="image" src="https://github.com/user-attachments/assets/ab34e163-5c65-4c71-99fd-6cadc6e76fed" />


---

## 🔹 2. Movies with Higher International Sales

```sql
SELECT movies.title, boxoffice.domestic_sales, boxoffice.international_sales
FROM movies
INNER JOIN boxoffice
ON movies.id = boxoffice.movie_id
WHERE boxoffice.international_sales > boxoffice.domestic_sales;
```
<img width="927" height="631" alt="image" src="https://github.com/user-attachments/assets/a8487cef-acb1-4406-838d-1b43a517b08f" />


---

## 🔹 3. Movies by Rating (Descending)

```sql
SELECT movies.title, boxoffice.rating
FROM movies
INNER JOIN boxoffice
ON movies.id = boxoffice.movie_id
ORDER BY boxoffice.rating DESC;
```
<img width="768" height="634" alt="image" src="https://github.com/user-attachments/assets/dcf152e5-9d5d-4102-a660-8ebb1b48fe95" />


---

## ⚙️ Key Concepts Used

| Concept    | Description                   |
| ---------- | ----------------------------- |
| INNER JOIN | Combines rows from two tables |
| ON         | Matching condition            |
| WHERE      | Filters data                  |
| ORDER BY   | Sorts results                 |
| DESC       | Highest to lowest             |

---

## 🚀 How to Run

1. Open SQLBolt or any SQL tool
2. Copy the queries
3. Execute them
4. Observe joined results

---

## 🌟 Features

✨ Multi-table queries
✨ Real-world database concept
✨ Beginner-friendly explanation
✨ Portfolio-ready SQL

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
JOIN table2 ON table1.id = table2.id
```

👉 Always join using a **common key**

---
