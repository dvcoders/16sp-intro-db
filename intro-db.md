class: middle, center

# intro-db
![db-image](./images/sqlite.gif)
---

# Agenda

1. Introduction with example
2. Types of databases
    - Relational and non relational
    - SQL
3. Workshop

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
	- Most use SQL (Structured Query Language)
	- Not very hip
	- Examples: Oracle, MySQL, SQLite

![relational-example](./images/relational-example.png) ![table-example](./images/table-example.png)

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

---

# Workshop Setup

1. Sign up at [heroku.com](https://www.heroku.com)
2. Grab the heroku toolbelt at [toolbelt.heroku.com](https://toolbelt.heroku.com)

```bash
$ heroku login
Enter your Heroku credentials.
Email: jesse@example.com
Password (typing will be hidden):
Authentication successful.

$ mkdir intro-db
$ cd intro-db
$ git init
Initialized empty Git repository in ./intro-db/.git/

$ heroku create
Creating app... done, stack is cedar-14
https://***.herokuapp.com/ | https://git.heroku.com/***.git

$ heroku addons:create heroku-postgresql:hobby-dev
Creating postgresql-trapezoidal-55564... done, (free)
Adding postgresql-trapezoidal-55564 to ***... done
Setting DATABASE_URL and restarting ***... done, v3
Database has been created and is available
 ! This database is empty. If upgrading, you can transfer
 ! data from another database with pg:copy
Use `heroku addons:docs heroku-postgresql` to view documentation.
```

---

# Workshop

1. Connect to the database

    ```bash
    $ heroku run 'psql $DATABASE_URL'
    Running psql $DATABASE_URL on ***.... up, run.1083
    psql (9.5.1, server 9.4.7)
    SSL connection (protocol: TLSv1.2, cipher: ..., bits: 256, compression: off)
    Type "help" for help.

    d2bh5qbs8qns39=> 
    ```
