# Practical 7 – Regression Analysis Using Python

## 📌 Project Overview

This practical focuses on Regression Analysis using Python and the Teaching Ratings Dataset. The main objective is to understand how different factors, such as gender, age group, and beauty score, are related to teaching evaluation scores.

The project uses Ordinary Least Squares (OLS) Regression and ANOVA to analyse relationships between variables and understand their statistical significance.

## 📂 Dataset Information

- **Dataset Name:** `TeachingRatings.csv`
- **Total Observations:** 463
- **Analysis Type:** Regression Analysis and ANOVA

### Dataset Features

The dataset contains information about professors, including:

- Age
- Gender
- Teaching Evaluation Score
- Beauty Score
- Tenure Status
- Minority Status
- Course Division
- Professor ID

## 🛠️ Technologies Used

- Python
- Pandas
- Statsmodels
- Google Colab / Jupyter Notebook

## 📦 Libraries Required

```python
import pandas as pd
import statsmodels.formula.api as smf
from statsmodels.stats.anova import anova_lm
```

Install the required libraries using:

```bash
pip install pandas statsmodels
```

## 🔍 Analysis Performed

### 1. Loading the Dataset

Loaded the `TeachingRatings.csv` file using Pandas to access and analyse professor evaluation data.

### 2. Q1 – Regression Analysis: Gender vs Teaching Evaluation Score

Performed OLS Regression to examine whether gender is related to teaching evaluation scores.

**Model Used:**

```python
model = smf.ols('eval ~ C(gender)', data=df).fit()
```

**Results:**

- Intercept: 3.9010
- Male Coefficient: 0.1680
- R-squared: 0.022
- F-statistic: 10.56
- P-value: 0.00124

**Hypotheses:**

- Null Hypothesis (H0): There is no significant difference in teaching evaluation scores between male and female instructors.
- Alternative Hypothesis (H1): There is a significant difference in teaching evaluation scores between male and female instructors.

**Decision:** Reject H0.

**Finding:** Since the p-value (0.00124) is less than 0.05, there is a statistically significant difference in teaching evaluation scores based on gender. Male instructors receive approximately 0.168 points higher evaluation scores than female instructors on average.

### 3. Q2 – ANOVA: Age Group vs Beauty Score

Divided professors into three age groups using their age:

- Young: Below 40 years
- Middle: 40–50 years
- Old: Above 50 years

Applied One-Way ANOVA to check whether average beauty scores differ across these age groups.

**Model Used:**

```python
model2 = smf.ols('beauty ~ C(age_group)', data=df).fit()
anova_table = anova_lm(model2)
```

**Results:**

- Sum of Squares: 17.8007
- F-statistic: 15.1890
- P-value: 0.0000004094

**Hypotheses:**

- Null Hypothesis (H0): There is no significant difference in beauty scores across the age groups.
- Alternative Hypothesis (H1): At least one age group has a significantly different average beauty score.

**Decision:** Reject H0.

**Finding:** Since the p-value is less than 0.05, there is a statistically significant difference in beauty scores across the age groups. This indicates that age groups have different average beauty scores.

### 4. Q3 – Regression Analysis: Beauty Score vs Teaching Evaluation Score

Performed OLS Regression to examine the relationship between professor beauty scores and teaching evaluation scores.

**Model Used:**

```python
model3 = smf.ols('eval ~ beauty', data=df).fit()
```

**Results:**

- Intercept: 3.9983
- Beauty Coefficient: 0.1330
- R-squared: 0.036
- F-statistic: 17.08
- P-value: 0.000

**Hypotheses:**

- Null Hypothesis (H0): There is no significant relationship between beauty score and teaching evaluation score.
- Alternative Hypothesis (H1): There is a significant relationship between beauty score and teaching evaluation score.

**Decision:** Reject H0.

**Finding:** Since the p-value is less than 0.05, there is a statistically significant positive relationship between beauty score and teaching evaluation score.

This means that when the beauty score increases by one unit, the predicted teaching evaluation score increases by approximately 0.133 points.

## 📊 Key Findings

- Gender is significantly related to teaching evaluation scores.
- Male instructors receive approximately 0.168 points higher average evaluation scores than female instructors.
- Beauty scores differ significantly across different age groups.
- Beauty score has a positive relationship with teaching evaluation score.
- A one-unit increase in beauty score is associated with an increase of approximately 0.133 points in the predicted evaluation score.
- The regression models have relatively low R-squared values, meaning that other factors also influence teaching evaluation scores.

## 📚 Statistical Methods Used

| Statistical Method | Purpose |
|---|---|
| OLS Regression | Examines the relationship between gender and evaluation scores. |
| ANOVA | Compares beauty scores across different age groups. |
| Simple Linear Regression | Examines the relationship between beauty score and evaluation score. |

## ▶️ How to Run This Project

1. Clone or download this GitHub repository.
2. Open the notebook in Google Colab or Jupyter Notebook.
3. Upload the `TeachingRatings.csv` dataset.
4. Install the required Python libraries.
5. Run all code cells in order.
6. Observe the regression summaries, ANOVA results, and conclusions.

## 📝 Conclusion

This practical demonstrates how Python can be used to perform regression analysis and ANOVA on real-world data.

Using Pandas and Statsmodels, we examined the relationship between gender and teaching evaluation scores, compared beauty scores across different age groups, and analysed the relationship between beauty score and teaching evaluation score.

The results show significant differences in evaluation scores based on gender and beauty scores across age groups. A positive relationship was also found between beauty score and teaching evaluation score.

Overall, this practical helps us understand how regression analysis and ANOVA can be used to identify relationships between variables and make data-based conclusions.

---

**Tools:** Python | Pandas | Statsmodels  
**Platform:** Google Colab  
**Project Type:** Data Science Practical – 7
