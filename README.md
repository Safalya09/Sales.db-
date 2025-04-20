# Sales.db-
# 🧾 Task 7: Basic Sales Summary using SQLite and Python

## 📌 Task Overview

This repository contains my submission for **Task 7: Basic Sales Summary from a Tiny SQLite Database** as part of the **Data Analyst Internship** program. The goal is to use SQL inside Python to extract sales data and display it using basic print statements and a simple bar chart.

## 🗃️ Dataset

A small SQLite database (`sales_data.db`) was created with a single table named `sales`.  
The table includes fields like:

- `product` (TEXT)
- `quantity` (INTEGER)
- `price` (REAL)

## ⚙️ Tools & Libraries Used

- Python
- SQLite (via `sqlite3`)
- Pandas
- Matplotlib
- Jupyter Notebook / Python script

## 📈 Task Steps

1. Created a database `sales_data.db` and inserted mock sales data.
2. Connected to the SQLite database using Python.
3. Ran SQL query to get total quantity and total revenue grouped by product:
   ```sql
   SELECT product, 
          SUM(quantity) AS total_qty, 
          SUM(quantity * price) AS revenue 
   FROM sales 
   GROUP BY product;

   1. How did you connect Python to a database?
Using the sqlite3 module with sqlite3.connect("sales_data.db").

2. What SQL query did you run?

sql
Copy
Edit
SELECT product, SUM(quantity) AS total_qty, SUM(quantity * price) AS revenue FROM sales GROUP BY product;
3. What does GROUP BY do?
GROUP BY is used to group rows that have the same values in specified columns and apply aggregate functions like SUM() to each group.

4. How did you calculate revenue?
By multiplying quantity * price and using SUM() to get total revenue per product.

5. How did you visualize the result?
Used matplotlib via df.plot(kind='bar', x='product', y='revenue').

6. What does pandas do in your code?
It helps in reading SQL query results into a DataFrame, manipulating data, and plotting charts easily.

7. What’s the benefit of using SQL inside Python?
It allows combining SQL querying power with Python’s flexibility and visualization capabilities — useful for automation and analysis.

8. Could you run the same SQL query directly in DB Browser for SQLite?
Yes, the same SQL query can be run directly in DB Browser, but Python offers more control and the ability to automate and visualize results.`
