# 🎯 SQL Bolt — Exercise 12 (GROUP BY + JOIN)

<p align="center">
  📊 Master SQL using <b>GROUP BY + JOIN + Aggregation</b>
</p>

---

## 📌 Overview

This exercise combines:

* 🔗 JOIN (multiple tables)
* 📊 GROUP BY (grouping data)
* ➕ Aggregation functions (COUNT, SUM)

---

## 🧠 Concepts Used

```sql
COUNT(*)
SUM(column)
GROUP BY column
JOIN table
```

💡 Used for analytics and reporting

---

## 📊 Tables Used

### 🎬 Movies

* id
* title
* director

### 💰 BoxOffice

* movie_id
* domestic_sales
* international_sales

---

# 📝 Exercise 12 — Solutions

---

## 🔹 1. Number of movies per director

```sql
SELECT director, COUNT(*) AS num_movies
FROM movies
GROUP BY director;
```
<img width="770" height="663" alt="image" src="https://github.com/user-attachments/assets/c992efec-fb65-43ed-8cbd-cb05581d1449" />


---

## 🔹 2. Total sales per director

```sql
SELECT movies.director,
       SUM(boxoffice.domestic_sales) AS total_domestic_sales,
       SUM(boxoffice.international_sales) AS total_international_sales
FROM movies
JOIN boxoffice
ON movies.id = boxoffice.movie_id
GROUP BY movies.director;
```
<img width="873" height="693" alt="image" src="https://github.com/user-attachments/assets/df9f8e8f-fc92-4d49-a3d2-daff974c6eed" />


---

## ⚙️ Key Concepts Used

| Concept  | Description     |
| -------- | --------------- |
| COUNT    | Counts rows     |
| SUM      | Adds values     |
| GROUP BY | Groups data     |
| JOIN     | Combines tables |

---

## 🚀 How to Run

```bash
1. Open SQLBolt or any SQL tool
2. Copy queries
3. Execute them
4. Analyze grouped results
```

---

## 🌟 Features

✨ Data aggregation + grouping
✨ Multi-table analysis
✨ Real-world reporting queries
✨ Beginner to intermediate level

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

👉 Required when using aggregation with non-aggregated columns

---
