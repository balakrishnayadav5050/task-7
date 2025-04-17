# task-7
Basic Sales Summary using SQLite and Python

## 🎯 Objective

Extract and summarize basic sales data from a SQLite database using Python. Generate a summary report and visualize revenue by product using a bar chart.

---

## 🛠 Tools & Libraries Used

- Python 3
- SQLite (via `sqlite3`)
- pandas
- matplotlib

---

## 🗃️ Dataset

A small SQLite database `sales_data.db` containing a `sales` table with the following fields:

- `id`: Auto-incremented ID
- `product`: Name of the product
- `quantity`: Units sold
- `price`: Price per unit

---

## 📌 Steps Performed

1. Created `sales_data.db` and a `sales` table.
2. Inserted sample sales records into the table.
3. Wrote SQL query to get:
   - Total quantity sold per product
   - Total revenue per product
4. Used pandas to run SQL and load results.
5. Printed sales summary using `print()`.
6. Visualized the revenue using a bar chart with matplotlib.

---

## 📊 Output

### Console Output
Printed a table of:
- Product name
- Total quantity sold
- Total revenue

### Chart
A bar chart saved as `sales_chart.png` showing **revenue by product**.

---

## 🧪 Example SQL Query

```sql
SELECT 
    product, 
    SUM(quantity) AS total_qty, 
    SUM(quantity * price) AS revenue 
FROM sales 
GROUP BY product;
