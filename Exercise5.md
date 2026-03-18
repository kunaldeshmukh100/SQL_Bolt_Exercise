# 🎯 SQL Bolt — Review 5 (Filtering & Sorting with Geography)

<p align="center">
  🌎 Work with real-world data using <b>WHERE, ORDER BY, LIMIT, OFFSET</b>
</p>

--- 

## 📌 Overview

This exercise focuses on **filtering and analyzing geographic data** using SQL.

You will learn how to:

* 🌍 Filter data by country
* 📊 Sort data using latitude & longitude
* 🔢 Find top cities using population
* ⏭ Use LIMIT & OFFSET for ranking

---

## 📊 Table Used: `north_american_cities`

| city                | country       | population | latitude  | longitude   |
| ------------------- | ------------- | ---------- | --------- | ----------- |
| Guadalajara         | Mexico        | 1500800    | 20.659699 | -103.349609 |
| Toronto             | Canada        | 2795060    | 43.653226 | -79.383184  |
| Houston             | United States | 2195914    | 29.760427 | -95.369803  |
| New York            | United States | 8405837    | 40.712784 | -74.005941  |
| Philadelphia        | United States | 1553165    | 39.952584 | -75.165222  |
| Havana              | Cuba          | 2106146    | 23.05407  | -82.345189  |
| Mexico City         | Mexico        | 8555500    | 19.432608 | -99.133208  |
| Phoenix             | United States | 1513367    | 33.448377 | -112.074037 |
| Los Angeles         | United States | 3884307    | 34.052234 | -118.243685 |
| Ecatepec de Morelos | Mexico        | 1742000    | 19.601841 | -99.050674  |
| Montreal            | Canada        | 1717767    | 45.501689 | -73.567256  |
| Chicago             | United States | 2718782    | 41.878114 | -87.629798  |

---

# 📝 Review 5 — Solutions

---

## 🔹 1. List all Canadian cities and their populations

```sql id="s4pt3x"
SELECT city, population
FROM north_american_cities
WHERE country = 'Canada';
```
<img width="639" height="597" alt="image" src="https://github.com/user-attachments/assets/7bf932b9-9425-4662-8787-1433badbcf02" />


---

## 🔹 2. Order all US cities by latitude (north → south)

```sql id="b1nnqf"
SELECT city
FROM north_american_cities
WHERE country = 'United States'
ORDER BY latitude DESC;
```
<img width="557" height="609" alt="image" src="https://github.com/user-attachments/assets/1ae6b3b7-b350-497f-a697-8602cf1297b8" />


💡 Higher latitude = more north

---

## 🔹 3. Cities west of Chicago (west → east)

📍 Chicago longitude: **-87.629798**

```sql id="qkp9fh"
SELECT city
FROM north_american_cities
WHERE longitude < -87.629798
ORDER BY longitude ASC;
```
<img width="437" height="634" alt="image" src="https://github.com/user-attachments/assets/62a943e3-7d47-4876-b051-d453e1356033" />


💡 More negative longitude = more west

---

## 🔹 4. Two largest cities in Mexico

```sql id="xtc9rf"
SELECT city, population
FROM north_american_cities
WHERE country = 'Mexico'
ORDER BY population DESC
LIMIT 2;
```
<img width="778" height="634" alt="image" src="https://github.com/user-attachments/assets/19f3eb5e-0ce8-43fc-a1eb-3432d32eaa92" />


---

## 🔹 5. 3rd & 4th largest US cities

```sql id="g5gcmk"
SELECT city, population
FROM north_american_cities
WHERE country = 'United States'
ORDER BY population DESC
LIMIT 2 OFFSET 2;
```
<img width="581" height="663" alt="image" src="https://github.com/user-attachments/assets/58e6215e-2246-404b-ac8e-8fb953282679" />



---

## ⚙️ Key Concepts Used

| Concept   | Description          |
| --------- | -------------------- |
| WHERE     | Filters rows         |
| ORDER BY  | Sorts results        |
| DESC      | Highest to lowest    |
| LIMIT     | Restricts results    |
| OFFSET    | Skips rows           |
| Latitude  | North/South position |
| Longitude | East/West position   |

---

## 🚀 How to Run

```bash
1. Open SQLBolt or any SQL tool
2. Copy the queries
3. Execute them
4. Compare results
```

---

## 🌟 Features

✨ Real-world dataset
✨ Geographic filtering
✨ Ranking queries
✨ Beginner-friendly explanations

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

```sql id="fov6mq"
ORDER BY latitude DESC   -- North → South
ORDER BY longitude ASC   -- West → East
LIMIT n                  -- Top results
OFFSET n                 -- Skip rows
```

---

