# 02 · Online Bookstore Analysis

Relational analysis of an online bookstore's data with pandas: joins, aggregations and schema normalization.

📓 [Notebook](notebook.ipynb) · 🌐 [HTML export](notebook.html)

## Tasks

| # | Task |
|---|------|
| 1 | Normalize the `orders` table (one order → many books) |
| 2 | Summary statistics for reviews |
| 3 | Increase prices for the Fiction category |
| 4 | Revenue by payment method |
| 5 | Count of Non-Fiction books |
| 6 | Average rating for orders placed on 19.11.2023 |
| 7 | Most expensive book in the Science category |
| 8 | Date, customer and books of the most recent orders |
| 9 | Most popular book by order frequency |
| 10 | Customers who spent more than €100 |
| 11 | Books that have never been ordered |
| 12 | Split customer name into first and last name |
| 13 | Add a new customer and an associated order |
| 14 | All books by J.K. Rowling |
| 15 | Restructure the book–category relationship into many-to-many |

**Techniques:** `merge`, `groupby` + `agg`, boolean filtering, string splitting, date filtering, building junction tables.

## Data

| File | Rows | Description |
|------|------|-------------|
| `data/books.csv` | 200 | Book catalog (title, author, price, category) |
| `data/categories.csv` | 5 | Book categories |
| `data/customers.csv` | 100 | Customers (name, email, phone) |
| `data/orders.csv` | 300 | Orders (date, customer, book, quantity, payment, total) |
| `data/reviews.csv` | 150 | Book reviews and ratings |
