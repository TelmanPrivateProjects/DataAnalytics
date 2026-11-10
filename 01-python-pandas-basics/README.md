# 01 · Python & Pandas Basics

An introduction to core Python, NumPy and pandas, ending with a hands-on data cleaning exercise.

📓 [Notebook](notebook.ipynb) · 🌐 [HTML export](notebook.html)

## Contents

1. **Python variables:** basic types and user input (`input()`).
2. **Strings:** formatting and string operations.
3. **Lists, sets, tuples, dictionaries:** includes a nested dictionary of books and a note on why a dictionary suits this data.
4. **NumPy:** array creation and vectorized operations.
5. **Pandas:** loading CSVs, finding a malformed row (semicolon separators in a comma-separated file) and cleaning a messy inventory dataset.

## Data cleaning steps (inventory dataset)

- Removed duplicate rows
- Filtered out rows with a zero `value`
- Coerced the `quantity` column to numeric and dropped invalid entries
- Dropped rows with missing values
- Reset the index and set appropriate column types

## Data

| File | Rows | Description |
|------|------|-------------|
| `data/employees.csv` | 50 | Employee records (HR-style schema) |
| `data/transactions.csv` | 10 | Customer transactions, including one malformed row |
| `data/inventory.csv` | 81 | Inventory records with deliberate quality issues |

> This notebook contains interactive `input()` cells. Run it in an interactive Jupyter session.
