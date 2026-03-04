# Technical Paper on Core Programming & Database Concepts

## 1. Arguments in Python

In Python, arguments are values passed to a function when it is called. They allow functions to operate on dynamic input.

### Types of Arguments:

- Positional Arguments

```bash
def add(a, b):
    return a + b
add(5, 3)
```

- Keyword Arguments

```bash
add(a=5, b=3)
```
- Default Arguments
```bash
def greet(name="Guest"):
    print(name)
```

## 2. UPDATE in SQL

The `UPDATE` statement modifies existing records in a table.
```bash
UPDATE students
SET marks = 90
WHERE id = 1;
```

- `SET`  specifies column to modify

- `WHERE`  specifies condition (very important to avoid updating all rows)

## 3. Use of NumPy

NumPy is a powerful Python library for numerical computing.

### Features:
- N-dimensional arrays (ndarray)

- Mathematical operations

- Linear algebra

- Random number generation

### Example:

```bash
import numpy as np
arr = np.array([1, 2, 3])
print(arr * 2)
```
## 4. Git and GitHub

- `Git` is a distributed version control system.

- `GitHub` is a cloud-based hosting platform for Git repositories.

## 5. Self Join in SQL

A self join joins a table with itself.

```bash
SELECT A.name, B.name AS manager
FROM employees A
JOIN employees B
ON A.manager_id = B.id;
```
## 6. touch Command in CLI

The `touch` command creates a new empty file.

```bash
touch file.txt
```
## 7. What is SQL?

SQL (Structured Query Language) is used to manage relational databases.

### Categories:

- DDL -> `CREATE`, `ALTER`, `DROP`

- DML -> `INSERT`, `UPDATE`, `DELETE`

- DQL -> `SELECT`

- DCL -> `GRANT`, `REVOKE`

## 8. ALTER in SQL

`ALTER` modifies table structure.

```bash
ALTER TABLE students
ADD email VARCHAR(100);
```
## 9. Slicing in Python

Slicing extracts a portion of a sequence.

```bash
s = "Python"
print(s[0:4])  # Pyth
```
 
## 10. Matplotlib in Python

`Matplotlib` is a data visualization library.

```bash
import matplotlib.pyplot as plt
plt.plot([1,2,3],[4,5,6])
plt.show()
```

## 11. Difference Between SQL and MongoDB

MongoDB is a NoSQL database.

| Feature        | SQL        | MongoDB     |
| -------------- | ---------- | ----------- |
| Type           | Relational | NoSQL       |
| Structure      | Tables     | Collections |
| Schema         | Fixed      | Flexible    |
| Query Language | SQL        | BSON/JSON   |


## 12. Difference Between ALTER and UPDATE

| ALTER                   | UPDATE       |
| ----------------------- | ------------ |
| Changes table structure | Changes data |
| DDL command             | DML command  |
| Affects columns         | Affects rows |


## 13. Order of Execution in SQL

1. FROM

2. JOIN

3. WHERE

4. GROUP BY

5. HAVING

6. SELECT

7. ORDER BY

8. LIMIT

## 14. Modulo (%) and Underscore (_) in SQL

Used in LIKE pattern matching:

```bash
SELECT * FROM users WHERE name LIKE '_a%';
```

- `_`  matches one character

- `%` matches multiple characters

## 15. Multiple Inheritance in Python

Multiple inheritance allows a class to inherit from more than one parent class.

```bash
class A:
    pass

class B:
    pass

class C(A, B):
    pass
```

## 16. Data Types of Variables

### Python:

- int

- float

- str

- bool

- list

- tuple

- set

- dict

### SQL:

- INT

- VARCHAR

- DATE

- BOOLEAN

- FLOAT

---
