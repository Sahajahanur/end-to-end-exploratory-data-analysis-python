# Exploratory Data Analysis (EDA) — Complete Framework with Python

A hands-on walkthrough of Exploratory Data Analysis covering **Univariate, Bivariate, and Multivariate analysis**, applied across four datasets (customer sales, news text, weather, daily sales) to learn how EDA techniques change based on variable type.

## Table of Contents
- [Overview](#overview)
- [What I Learned](#what-i-learned)
- [Datasets Used](#datasets-used)
- [Tools & Tech](#tools--tech)
- [Analysis Pipeline](#analysis-pipeline)
- [Key Takeaways](#key-takeaways)
- [Full Report](#full-report)
- [Author & Contact](#author--contact)

## Overview
Most beginners think EDA just means `.describe()`, `.shape`, and a couple of histograms — and that's exactly why their downstream insights and models turn out inaccurate. This lesson breaks EDA down into its three real analytical layers — **Univariate → Bivariate → Multivariate** — and shows, with working code, when and why each technique is used depending on the variable type (numeric, categorical, datetime, or text).

## What I Learned
- **Univariate analysis** differs by variable type: numeric needs summary stats + distribution plots (histogram, boxplot, density), categorical needs frequency counts + cardinality checks, datetime needs range/gap/granularity checks + seasonality, and text needs token counts + word frequency after stopword removal.
- **Bivariate analysis** is about relationships: numeric-numeric uses correlation + scatter/regression, numeric-categorical uses grouped boxplots + ANOVA, categorical-categorical uses contingency tables + Chi-Square test, and time series pairs use lag plots + ACF/PACF.
- **Multivariate analysis** looks at how 2+ features jointly influence a target — via interaction plots, and how PCA + KMeans can be combined to reduce dimensions and discover natural customer segments.
- A single, reusable EDA workflow (data type audit → univariate → bivariate → multivariate) can be applied to virtually any tabular dataset before modeling.
- Statistical significance checks (ANOVA, Chi-Square) matter — visual differences aren't always statistically meaningful.

## Datasets Used
| Dataset | Used For |
|---|---|
| `cleaned_customer_sales.csv` | Numeric, categorical & datetime analysis |
| `fake_or_real_news.csv` | Text variable analysis |
| `weather.csv` | Numeric-numeric correlation & regression |
| `daily_sales_data.csv` | Time series relationship analysis |

## Tools & Tech
Python 3 · pandas · matplotlib · seaborn · scipy.stats · statsmodels · nltk · scikit-learn (StandardScaler, PCA, KMeans)

## Analysis Pipeline
```
Raw CSV → Data Type Audit → Datetime Conversion
        → Univariate Analysis (Numeric | Categorical | Datetime | Text)
        → Bivariate Analysis (Numeric-Numeric | Numeric-Categorical | Categorical-Categorical | Time Series)
        → Multivariate Analysis (Interaction Plots | PCA | KMeans Clustering)
        → Insights & Next Steps
```

## Key Takeaways
- No significant outliers found in customer sales numeric columns; distribution fairly uniform across Gender and City.
- ANOVA and Chi-Square tests both returned p-value > 0.05 → no statistically significant group differences in this dataset.
- News dataset text was politics/election-focused based on top word frequencies after stopword removal.
- Temperature and Apparent Temperature showed strong positive correlation (~0.9) in the weather dataset.
- Daily sales showed no meaningful autocorrelation at lag-1 or lag-7.
- KMeans on PCA-reduced customer data revealed two clear segments differentiated mainly by Purchase Amount and Feedback Score.

## Full Report
A complete, cell-by-cell code walkthrough with explanations, outputs, and insights is available in **`EDA_Report.pdf`**.

## Author & Contact
**Sahajahanur Rahman**
Email: connectingsrl@gmail.com
GitHub: [Sahajahanur](https://github.com/Sahajahanur)
