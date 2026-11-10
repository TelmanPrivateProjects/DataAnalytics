# Data Analytics with Python

A collection of five data analytics projects in Python. They go from language basics and data cleaning to visualization, hypothesis testing and regression modeling. Each project is a self-contained Jupyter notebook with its dataset and a pre-rendered HTML export.

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?logo=jupyter&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?logo=numpy&logoColor=white)
![seaborn](https://img.shields.io/badge/seaborn-4C72B0)
![SciPy](https://img.shields.io/badge/SciPy-8CAAE6?logo=scipy&logoColor=white)
![statsmodels](https://img.shields.io/badge/statsmodels-4051B5)
![scikit--learn](https://img.shields.io/badge/scikit--learn-F7931E?logo=scikitlearn&logoColor=white)

## Projects

| # | Project | Topics | Key techniques |
|---|---------|--------|----------------|
| 01 | [Python & Pandas Basics](01-python-pandas-basics/) | Python data structures, NumPy, data cleaning | Lists/dicts/sets, NumPy arrays, deduplication, type coercion, NaN handling |
| 02 | [Online Bookstore Analysis](02-online-bookstore-analysis/) | Relational data with pandas | Joins, `groupby` aggregations, normalization (1:N to N:M), filtering |
| 03 | [Real Estate Visualization](03-real-estate-visualization/) | Exploratory data analysis | Histogram, KDE, ECDF, box/joint/relational/faceted plots, outlier detection |
| 04 | [TechGadgets Hypothesis Testing](04-techgadgets-hypothesis-testing/) | Inferential statistics | Levene's test, independent t-test, Welch's ANOVA, chi-square test |
| 05 | [EduLearn Regression Analysis](05-edulearn-regression-analysis/) | Correlation & predictive modeling | Pearson correlation, heatmap, multiple OLS regression, MAE/RMSE/R² |

## Highlights

- **TechGadgets:** Delivery time has no significant effect on profit (t-test, p = 0.47). Profit does differ significantly across gadget types (Welch's ANOVA, p ≈ 3.2e-13): laptops average about 81 per sale, tablets about 19 and smartphones about 8. Customer segment and smartphone purchases are independent (χ², p = 0.71).
- **EduLearn:** Marketing spend is the strongest driver of course enrollment (r ≈ 0.78). A multiple regression model explains about 63% of the variance in enrollment (R² = 0.631), and instructor rating is the other key predictor.
- **Real Estate:** A cleaning pipeline (median imputation, logical consistency checks, categorical typing) is followed by 13 visualizations of price, age, fee and tax distributions across property types and locations.

## Repository structure

```
.
├── 01-python-pandas-basics/
│   ├── README.md          # project summary
│   ├── notebook.ipynb     # analysis notebook
│   ├── notebook.html      # rendered export (view without Jupyter)
│   └── data/              # input CSV files
├── 02-online-bookstore-analysis/
├── 03-real-estate-visualization/
├── 04-techgadgets-hypothesis-testing/
├── 05-edulearn-regression-analysis/
└── requirements.txt
```

## Getting started

```bash
git clone https://github.com/TelmanPrivateProjects/DataAnalytics.git
cd DataAnalytics

python3 -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate
pip install -r requirements.txt

jupyter lab
```

Open a project folder and run `notebook.ipynb`. Each notebook loads its data from its own `data/` folder with relative paths, so start Jupyter from the repository root or from the project folder.

> **Note:** The notebooks were written against **pandas 2.x**. pandas 3 changes how string columns are handled, which alters some cleaning results, so `requirements.txt` pins `pandas<3`.
>
> Project 01 contains interactive `input()` cells, so run it in an interactive Jupyter session.

To see the results without installing anything, open the `notebook.html` file in any project folder.
