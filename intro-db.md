class: middle, center

# intro-db
![db-image](./images/sqlite.gif)
---

# Agenda

1. -
2. -
3. -

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
# Introduction

- Understanding databases is a big plus when finding internships - many ask for some knowledge of SQL
- Database Management Systems (DBMS) - Software that allows access to a database
- "Database" may refer to the both the data and the DBMS
- DBMSs structure data according to different models
- DBMSs use different querying languages to access data
	- SQL is the most popular, and is used with many DBMSs
	- Others use their own query languages

![dbms](./images/dbms.png)

---

# Relational Databases

- Use tables of columns and rows to represent data
	- Relate tables together using keys
	- Most use SQL (Standard Query Language)
	- Not very hip
	- Examples: Oracle, MySQL, SQLite

![relational-example](./images/relational-example.png)

---

# NoSQL Databases

- A broad term referring to databases that do not use the relational table model

- Key-Value Stores
	- Act similarly to a hash table
	- Records can hold different types of data
	- Examples: Redis, Amazon DynamoDB

![key-value-example](./images/key-value-example.png)

---

# NoSQL Databases
- Document Stores 
	- Similar to key-value stores - items may have different structures
	- can have a nested structure, like JSON
	- useful for holding arrays
	- Examples: MongoDB, RethinkDB

![document-store-example](./images/document-store-example.png)
