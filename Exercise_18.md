# 🎯 SQL Bolt — Exercise 18 (DROP TABLE)

<p align="center">
  🗑️ Learn how to <b>remove entire tables</b> from a database
</p>

---

## 📌 Overview

This exercise focuses on:

* 🗑️ Dropping tables
* 🧹 Cleaning up database
* ⚠️ Understanding destructive operations

---

## 🧠 Concepts Covered

✔ DROP TABLE
✔ IF EXISTS
✔ Database cleanup

---

## 📝 Exercise 18 — Tasks

1. Remove the **Movies** table
2. Remove the **BoxOffice** table

---

## ✅ Solutions

```sql
DROP TABLE IF EXISTS movies;
```


<img width="790" height="561" alt="image" src="https://github.com/user-attachments/assets/ba4a912c-36be-4b69-89aa-ea66c7bc6136" />

```




DROP TABLE IF EXISTS boxoffice;
```


<img width="732" height="532" alt="image" src="https://github.com/user-attachments/assets/470a41ef-f8e6-44ac-81b3-f442e36adb0c" />


---

## ⚙️ Syntax Used

```sql
DROP TABLE IF EXISTS table_name;
```

---

## ⚠️ Important Notes

🚨 This operation is **permanent**

❌ You CANNOT recover:

* Data
* Structure

---

## 🚀 How to Run

1. Open SQLBolt / MySQL / SQLite
2. Run DROP queries
3. Verify tables are removed

---

## 🌟 Features

✨ Database cleanup
✨ Final SQL operation
✨ Beginner-friendly
✨ GitHub portfolio ready

---

## 👨‍💻 Author

**Kunal Deshmukh**

---

## ⭐ Support

If you liked this:

⭐ Star the repo
🚀 Share with others
📘 Keep learning SQL

---

## 💬 Pro Tip

👉 Always double-check before dropping:

```sql
SELECT * FROM movies;
```

---
