# 03 · Real Estate Visualization

Exploratory data analysis of a real estate agency's property listings with seaborn and matplotlib.

📓 [Notebook](notebook.ipynb) · 🌐 [HTML export](notebook.html)

## 1. Data cleaning & measurement scales

- Median imputation for missing `Age`
- Removed rows with missing or zero `Price` and removed duplicates
- Standardized text columns (`SaleStatus`, `Location`, `Type`) and converted them to `category`
- Logical consistency checks: no negative age, positive size/tenure, tax below price, at least one room
- Classified every attribute as nominal, ordinal or ratio

## 2. Visualizations

| # | Question | Chart |
|---|----------|-------|
| 2.1 | Age distribution | Histogram (`displot`) |
| 2.2 | Age by location | Box plot |
| 2.3 | Price density | KDE |
| 2.4 | Price density by performance rating | KDE with `hue` |
| 2.5 | Monthly HOA fees: proportions and thresholds | ECDF |
| 2.6 | Price vs age | Joint plot |
| 2.7 | Price vs days listed, by type | Faceted scatter (`relplot`) |
| 2.8 | Annual property tax by start year | Categorical box plot |
| 2.9 | Price by type and location | Grouped box plot |
| 2.10–2.11 | Price outliers by property type | Box plot |
| 2.12 | Rooms & bathrooms vs price | Scatter with color encoding |
| 2.13 | Average price by type across locations | Faceted bar plot |

## Data

| File | Rows | Description |
|------|------|-------------|
| `data/RealEstate_Data.csv` | 5,005 | Property listings: age, location, type, rooms, size, price, HOA fees, tax, rating, days listed, tenure |
