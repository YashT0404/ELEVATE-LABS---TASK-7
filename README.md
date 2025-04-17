# 🧾 Task 7 - Basic Sales Summary using SQLite & Python

## 📌 Overview

In this task, we were asked to create a basic sales summary from a small SQLite database using SQL within Python. The task focused on:
- Connecting to a SQLite database
- Running SQL queries to summarize sales
- Displaying the results using print statements and a bar chart

---

## 📂 Dataset

The dataset contains the following columns:
- `order_id`: Unique ID for each order
- `order_item_id`: The item number in the order
- `product_id`: The unique ID of the product
- `seller_id`: The seller responsible for the order
- `price`: Price of the product for that order item

The data was stored in a CSV file (`sales_data.csv`) and loaded into a SQLite database (`sales_data.db`) for analysis.

---

## 🛠 Tools Used
- Python
- SQLite3 (built-in in Python)
- Pandas
- Matplotlib

---

## 🔍 SQL Query Used

```sql
SELECT 
    product_id, 
    COUNT(*) AS total_items_sold,
    SUM(price) AS total_revenue
FROM sales
GROUP BY product_id
ORDER BY total_revenue DESC;
