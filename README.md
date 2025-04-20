# Task-7-Sales-Summary
# 🧩 Task 7 – Basic Sales Summary using SQLite and Python

## 🎯 Objective
This task demonstrates how to use SQL inside Python to pull basic sales insights — such as total quantity sold and total revenue — and display the results using both print statements and a simple bar chart.

---

## 🛠 Tools Used
- Python
- SQLite (via sqlite3)
- Pandas
- Matplotlib

---

## 📂 Files in this Repository

| File | Description |
|------|-------------|
| `task7_script.py` | Python script that connects to the database, runs SQL queries, prints summary, and generates a chart |
| `sales_data.db`   | SQLite database with a table named `sales` containing product, quantity, and price data |
| `sales_chart.png` | A simple bar chart showing revenue by product |
| `sales_data.csv`  | 🔹 Easy-to-open Excel/CSV version of the data (for non-technical viewers) |
| `README.md`       | This file, explaining the project and its contents |

---

## 🧪 What the Script Does

1. Connects to `sales_data.db`
2. Executes a SQL query to calculate:
   - Total quantity sold per product
   - Total revenue per product
3. Loads results into a DataFrame
4. Prints the summary using `print()`
5. Visualizes revenue using a bar chart (saved as `sales_chart.png`)

### 📊 Sample SQL Query Used

```sql
SELECT 
    product, 
    SUM(quantity) AS total_qty, 
    SUM(quantity * price) AS revenue 
FROM sales 
GROUP BY product;
