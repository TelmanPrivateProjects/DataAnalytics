# 05 · EduLearn Regression Analysis

Correlation and multiple linear regression analysis to find what drives course enrollment on an online education platform.

📓 [Notebook](notebook.ipynb) · 🌐 [HTML export](notebook.html)

## Workflow

1. **Cleaning:** date conversion, deduplication, median imputation, text standardization, logical range filters (e.g. rating ≤ 5, score ≤ 100).
2. **Correlation analysis:** Pearson correlations with `Enrollment`, a heatmap and a scatter plot of the strongest relationship.
3. **Regression:** an OLS model (`statsmodels`) with six predictors, evaluated with MAE, MSE, RMSE and R², then refined by removing non-significant predictors.
4. **Insights:** recommendations, limitations and directions for further research.

## Key results

| Metric | Value |
|--------|-------|
| Strongest correlate | `Marketing_Spend` (r ≈ 0.78) |
| R² (full model) | 0.631 |
| MAE / RMSE | ≈ 180 / ≈ 227 students |
| Significant predictors | `Marketing_Spend`, `Instructor_Rating`, `Duration_Weeks`, `Prerequisite_Score` |
| Not significant | `Price_USD`, `Completion_Rate` |

**Takeaway:** Marketing investment and instructor quality are the main levers for raising enrollment. A 1-point increase in instructor rating is associated with about 204 more enrollments.

## Data

| File | Rows | Description |
|------|------|-------------|
| `data/edulearn_dataset.csv` | 2,200 | Courses: launch date, category, duration, price, marketing spend, instructor rating, prerequisite score, enrollment, completion rate, external factors |
