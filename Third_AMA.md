
This document explains some important concepts related to **JavaScript, CLI, CSS,** and **SQL**.

---

# 1. Scope of `let` Variable

In JavaScript, `let` is used to declare variables with **block scope**.

### Key Points

* A variable declared with `let` is only accessible **inside the block `{}` where it is defined**.

### Example

```javascript
if (true) {
  let message = "Hello World";
  console.log(message); // Works
}

console.log(message); // Error: message is not defined
```
---

# 2. What is CLI (Command Line Interface)

CLI is a **text-based interface used to interact with the operating system by typing commands**.

Instead of clicking buttons, users type commands in a terminal.

### Examples of CLI tools

* Linux Terminal
* Windows Command Prompt
* Mac Terminal

### Example command

```bash
ls
```

Lists files in the current directory.

---

# 3. Searching a Pattern in a File using CLI

In Linux, the `grep` command is used to search for a pattern inside a file.

### Syntax

```bash
grep "pattern" filename
```

### Example

```bash
grep "error" log.txt
```

This command searches the word **error** inside `log.txt`.

### Useful Options

| Command   | Description      |
| --------- | ---------------- |
| `grep -i` | Ignore case      |
| `grep -n` | Show line number |
| `grep -r` | Recursive search |

---

# 4. Common Table Expression (CTE)

A **Common Table Expression** is a temporary result set that you can reference inside a SQL query.

It is created using the `WITH` keyword.

### Example

```sql
WITH EmployeeSalary AS (
    SELECT name, salary
    FROM employees
)
SELECT * FROM EmployeeSalary;
```

### Advantages

* Improves readability
* Simplifies complex queries
* Can be reused in the same query

---

# 5. Can We Use HAVING Without GROUP BY?

Yes, **HAVING can be used without GROUP BY**, but it behaves like a `WHERE` clause for aggregated results.

### Example

```sql
SELECT COUNT(*) 
FROM employees
HAVING COUNT(*) > 5;
```

This checks if total rows are greater than 5.

---

# 6. Default Flex Direction

In CSS Flexbox, the default direction is:

```css
flex-direction: row;
```

### Meaning

Items are placed **horizontally from left to right**.

### Other options

* `row`
* `row-reverse`
* `column`
* `column-reverse`

Example:

```css
.container{
display:flex;
flex-direction:column;
}
```

---

# 7. What is a Foreign Key

A **foreign key** is a column in a table that references the **primary key of another table**.

It is used to maintain **relationships between tables**.

### Example

**Students Table**

| id | name |
| -- | ---- |
| 1  | Ali  |

**Orders Table**

| order_id | student_id |
| -------- | ---------- |
| 101      | 1          |

Here:

```
student_id -> foreign key
```

---

# 8. `fr` in Grid

`fr` means **fractional unit** used in CSS Grid.

It divides available space proportionally.

### Example

```css
grid-template-columns: 1fr 2fr;
```

Meaning:

* First column takes **1 part**
* Second column takes **2 parts**

So second column becomes **twice the size**.

Note: `fr` works in **CSS Grid**, not in Flexbox.

---

# 9. Background Repeat Property

The `background-repeat` property controls how a background image repeats.

### Syntax

```css
background-repeat: repeat;
```

### Values

| Value     | Description                   |
| --------- | ----------------------------- |
| repeat    | image repeats both directions |
| repeat-x  | repeats horizontally          |
| repeat-y  | repeats vertically            |
| no-repeat | image appears only once       |

### Example

```css
body{
background-image:url("image.jpg");
background-repeat:no-repeat;
}
```

---

# 10. NOT NULL Constraint

`NOT NULL` ensures that a column **cannot contain NULL values**.

### Example

```sql
CREATE TABLE users (
    id INT,
    name VARCHAR(50) NOT NULL
);
```

Here the **name column must have a value**.

---

# 11. What is a View in SQL

A **View** is a virtual table based on the result of a SQL query.

It does not store data physically.

### Example

```sql
CREATE VIEW employee_view AS
SELECT name, salary
FROM employees;
```

You can query it like a normal table:

```sql
SELECT * FROM employee_view;
```

### Advantages

* Simplifies complex queries
* Improves security
* Provides abstraction

---

# 12. Why We Use JOIN in SQL

`JOIN` is used to combine rows from **two or more tables** based on a related column.

### Types of JOIN

| Join Type  | Description                       |
| ---------- | --------------------------------- |
| INNER JOIN | Returns matching rows             |
| LEFT JOIN  | Returns all rows from left table  |
| RIGHT JOIN | Returns all rows from right table |
| FULL JOIN  | Returns all rows from both tables |

### Example

```sql
SELECT students.name, orders.order_id
FROM students
INNER JOIN orders
ON students.id = orders.student_id;
```

---

# 13. Use of Border Radius

`border-radius` is used to create **rounded corners** for elements.

### Example

```css
.box{
border-radius:10px;
}
```

### Result

Corners of the element become rounded.

### Circle Example

```css
.circle{
width:100px;
height:100px;
border-radius:50%;
}
```

Creates a **circle shape**.

---

# 14. Gap in CSS

`gap` defines the **space between items in Grid or Flex layouts**.

### Example

```css
.container{
display:flex;
gap:20px;
}
```

This creates **20px space between items**.

### Grid Example

```css
.container{
display:grid;
grid-template-columns:1fr 1fr;
gap:10px;
}
```

### Advantages

* Cleaner than using margins
* Works in both **Flexbox and Grid**

---
