# 🎯 SQL Bolt — Exercise 3 (Pattern Matching)

<p align="center">
  🔍 Learn SQL filtering using <b>LIKE, NOT, and text matching</b>
</p>

--- 

## 📌 Overview

This exercise focuses on **filtering text data** using SQL conditions.

You will learn how to:

* 🔎 Search text using `LIKE`
* 🎯 Filter specific patterns
* ❌ Exclude results using `NOT`
* 📊 Combine conditions with columns

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
| 87 | WALL-G              | Brenda Chapman | 2042 | 97             |

---

# 📝 Exercise 3 — Solutions

---

## 🔹 1. Find all the Toy Story movies

```sql
SELECT *
FROM movies
WHERE title LIKE 'Toy Story%';
```
<img width="787" height="589" alt="image" src="https://github.com/user-attachments/assets/fff658e4-bf3f-47da-a4ed-dac3677dcbc3" />


💡 Matches:

* Toy Story
* Toy Story 2
* Toy Story 3

---

## 🔹 2. Find all movies directed by John Lasseter

```sql
SELECT *
FROM movies
WHERE director = 'John Lasseter';
```
<img width="840" height="601" alt="image" src="https://github.com/user-attachments/assets/ac70b7b8-7367-4ddb-8cde-96787e7ee677" />


---

## 🔹 3. Find all movies NOT directed by John Lasseter

```sql
SELECT title, director
FROM movies
WHERE director != 'John Lasseter';
```
<img width="703" height="589" alt="image" src="https://github.com/user-attachments/assets/6ea84ce6-675e-473b-92d8-c394525231ad" />


💡 `!=` means NOT EQUAL

---

## 🔹 4. Find all the WALL-* movies

```sql
SELECT *
FROM movies
WHERE title LIKE 'WALL-%';
```
<img width="798" height="622" alt="image" src="https://github.com/user-attachments/assets/0cb52a89-f23c-40a1-8f6b-4d88a3d18860" />



💡 Matches:

* WALL-E
* WALL-G

---

## ⚙️ Key Concepts Used

| Concept | Description               |
| ------- | ------------------------- |
| LIKE    | Pattern matching          |
| %       | Wildcard (any characters) |
| =       | Exact match               |
| !=      | Not equal                 |
| WHERE   | Filtering condition       |

---

## 🚀 How to Run

1. Open SQLBolt or any SQL tool
2. Copy the queries
3. Execute them
4. Compare results

---

## 🌟 Features

✨ Pattern matching queries
✨ Real dataset examples
✨ Beginner-friendly explanations
✨ GitHub-ready structure

---

## 👨‍💻 Author

**Kunal Deshmukh**

---

## ⭐ Support

If you found this helpful:

* ⭐ Star the repo
* 🔁 Share with friends
* 🚀 Keep learning SQL

---

## 💬 Tip

`LIKE 'text%'` → starts with
`LIKE '%text'` → ends with
`LIKE '%text%'` → contains

---

