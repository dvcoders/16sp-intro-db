class: middle, center

# intro-db
![db-image](./images/sqlite.gif)
---

# Agenda

1. -
2. -
3. -

---

# Introduction

---

# An Example

![dvc-schedule](./images/dvc-schedule.png)

---

# An Example

- Problem: storing information about 70,000 lines worth of DVC courses in a text file is inefficient, hard to manage, and slow at insertion, updating, and retrieval

- Parsing the file, then storing the information in data structures such as hash tables is not great, becuase all that information is stored in RAM

- Facebook stores 300 PB of data, an impossible amount to store in RAM

- Updating information requires writing to the file

- Many applications may want to access the data at one time

---

# Relational Databases

- Use tables of columns and rows to represent data
	- Relate tables together using keys
	- Most use SQL (Standard Query Language)
	- Not very hip
	- Examples: Oracle, MySQL, SQLite

![relational-example](./images/relational-example.png)

---
