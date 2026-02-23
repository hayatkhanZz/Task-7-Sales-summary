# Task-7-Sales-summary
basic Sales summary to pull simple sales info and display it using basic print statements and a simple bar chart 

## Project Overview
This project demonstrates how to use Python with SQLite to perform basic SQL queries and visualize sales data. 
 
A small SQLite database (sales_data.db) was created containing a single table named sales.

The project includes:
- Connecting to a SQLite database using Python
- Running SQL queries with GROUP BY
- Calculating total quantity and revenue
- Loading query results into pandas
- Displaying output using print()
- Creating a basic matplotlib bar chart

---

## Dataset
A small SQLite database file named sales_data.db was created with one table:

### Table: sales

| Column   | Data Type |
|----------|----------|
| product  | TEXT     |
| quantity | INTEGER  |
| price    | REAL     |

Sample sales data was inserted to perform analysis.

---

## Technologies Used
- Python
- SQLite (sqlite3)
- Pandas
- Matplotlib
- Google Colab

---

## SQL Query Used

```sql
SELECT product,
       SUM(quantity) AS total_qty,
       SUM(quantity * price) AS revenue
FROM sales
GROUP BY product;
```
