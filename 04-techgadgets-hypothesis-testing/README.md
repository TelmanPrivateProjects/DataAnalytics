# 04 · TechGadgets Hypothesis Testing

Statistical hypothesis testing on a gadget retailer's sales data to find what drives profit.

📓 [Notebook](notebook.ipynb) · 🌐 [HTML export](notebook.html)

## 1. Data cleaning

Converted dates to datetime, removed duplicates and rows delivered before they were purchased, dropped missing `Profit`, standardized and categorized text columns, and kept only profit values between -6,000 and 10,000.

## 2. Hypothesis tests

| # | Question | Test | Result | Conclusion |
|---|----------|------|--------|------------|
| 2.1 | Does delivery time (≤ 6 vs > 6 days) affect profit? | Levene + independent t-test | p = 0.470 | No significant difference |
| 2.2 | Do smartphones differ in profit from other gadget types? | Levene + t-test (unequal variances) | p ≈ 1.7e-11 | Significant difference |
| 2.3 | Does profit differ across all gadget types? | Levene + Welch's ANOVA | F = 28.99, p ≈ 3.2e-13 | Significant: Laptop ≈ 81.3, Tablet ≈ 19.4, Smartphone ≈ 7.8 mean profit |
| 2.4 | Is customer segment associated with smartphone purchases? | Chi-square test of independence | χ² = 0.14, p = 0.709 | Independent |

**Takeaway:** Gadget type matters for profit and delivery speed does not. Premium and non-premium customers buy smartphones at the same rate.

## Data

| File | Rows | Description |
|------|------|-------------|
| `data/techgadgets_data.csv` | 9,994 | Orders: purchase/delivery dates, customer segment, location, gadget type, profit |
