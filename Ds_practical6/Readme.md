# Practical 6 – Statistical Tests Using Python

## 📌 Project Overview

This project focuses on performing statistical tests using Python on the Teaching Ratings Dataset. The main objective is to understand the relationship between different variables and identify whether differences or associations are statistically significant.

The practical includes T-test, ANOVA, Chi-square test, and Correlation analysis using Pandas and SciPy.

## 📂 Dataset Information

- **Dataset Name:** `TeachingRatings.csv`
- **Total Observations:** 463
- **Total Columns:** 13

### Dataset Features

The dataset contains information about professors, including:

- Age
- Gender
- Minority Status
- Teaching Evaluation Scores
- Beauty Ratings
- Course Credits
- Course Division
- Native English Speaker Status
- Tenure Status
- Number of Students
- Professor ID

## 🛠️ Technologies Used

- Python
- Pandas
- SciPy
- Google Colab / Jupyter Notebook

## 📦 Libraries Required

```python
import pandas as pd
from scipy import stats
```

Install the required libraries using:

```bash
pip install pandas scipy
```

## 🔍 Analysis Performed

### 1. Loading the Dataset

Loaded the `TeachingRatings.csv` file using Pandas to access and analyse professor evaluation data.

### 2. Q1 – T-test: Does Gender Affect Teaching Evaluation Scores?

Performed an independent two-sample T-test to compare the average teaching evaluation scores of male and female professors.

**Results:**

- Male Mean Evaluation: 4.0690
- Female Mean Evaluation: 3.9010
- Male Sample Size: 268
- Female Sample Size: 195
- T-statistic: 3.2667
- P-value: 0.0012

**Hypotheses:**

- Null Hypothesis (H0): There is no significant difference in teaching evaluation scores between male and female professors.
- Alternative Hypothesis (H1): There is a significant difference in teaching evaluation scores between male and female professors.

**Decision:** Reject H0.

**Finding:** Since the p-value (0.0012) is less than 0.05, there is a statistically significant difference in teaching evaluation scores between male and female professors. Male professors have a higher average evaluation score in this dataset.

### 3. Q2 – ANOVA: Does Beauty Score Differ by Age Group?

Divided professors into four age groups and performed a One-Way ANOVA test to compare their average beauty scores.

**Age Groups and Results:**

| Age Group | Average Beauty Score | Sample Size |
|---|---:|---:|
| Young (29–42) | 0.3426 | 136 |
| Middle (43–48) | -0.1051 | 97 |
| Upper-Middle (49–57) | -0.1049 | 136 |
| Senior (58–73) | -0.2354 | 94 |

**Test Results:**

- F-statistic: 13.7820
- P-value: 0.0000

**Hypotheses:**

- Null Hypothesis (H0): There is no significant difference in average beauty scores across the age groups.
- Alternative Hypothesis (H1): At least one age group has a significantly different average beauty score.

**Decision:** Reject H0.

**Finding:** Since the p-value is less than 0.05, there is a statistically significant difference in beauty scores across the age groups. The young age group has the highest average beauty score, while the senior group has the lowest.

### 4. Q3 – Chi-square Test: Is There an Association Between Tenure and Gender?

Performed a Chi-square test of independence to examine whether gender and tenure status are associated.

**Contingency Table:**

| Gender | No Tenure | Tenure |
|---|---:|---:|
| Female | 50 | 145 |
| Male | 52 | 216 |

**Test Results:**

- Chi-square Statistic: 2.2068
- Degrees of Freedom: 1
- P-value: 0.1374

**Hypotheses:**

- Null Hypothesis (H0): There is no significant association between gender and tenure status.
- Alternative Hypothesis (H1): There is a significant association between gender and tenure status.

**Decision:** Fail to Reject H0.

**Finding:** Since the p-value (0.1374) is greater than 0.05, there is no statistically significant association between gender and tenure status in this dataset.

### 5. Q4 – Correlation: Is Evaluation Score Correlated with Beauty Score?

Used Pearson's correlation test to examine the relationship between professors' beauty scores and teaching evaluation scores.

**Results:**

- Pearson's Correlation Coefficient (r): 0.1890
- P-value: 0.0000

**Hypotheses:**

- Null Hypothesis (H0): There is no significant correlation between beauty score and evaluation score.
- Alternative Hypothesis (H1): There is a significant correlation between beauty score and evaluation score.

**Decision:** Reject H0.

**Finding:** The correlation coefficient of 0.1890 indicates a very weak positive relationship between beauty score and teaching evaluation score. Since the p-value is less than 0.05, this relationship is statistically significant.

## 📊 Key Findings

- Male professors have a higher average teaching evaluation score than female professors in this dataset.
- There is a statistically significant difference in teaching evaluation scores between male and female professors.
- Beauty scores differ significantly across age groups.
- The young age group has the highest average beauty score.
- There is no statistically significant association between gender and tenure status.
- Beauty score and teaching evaluation score have a very weak positive correlation.
- The correlation between beauty and evaluation scores is statistically significant.

## 📚 Statistical Tests Used

| Statistical Test | Purpose |
|---|---|
| T-test | Compares the average evaluation scores of male and female professors. |
| ANOVA | Compares beauty scores across different age groups. |
| Chi-square Test | Checks the association between gender and tenure status. |
| Pearson Correlation | Measures the relationship between beauty and evaluation scores. |

## ▶️ How to Run This Project

1. Clone or download this GitHub repository.
2. Open the notebook in Google Colab or Jupyter Notebook.
3. Upload the `TeachingRatings.csv` dataset.
4. Install the required Python libraries.
5. Run all code cells.
6. Observe the statistical results and decisions.

## 📝 Conclusion

This practical demonstrates how Python can be used to perform different statistical tests and analyse relationships between variables.

Using Pandas and SciPy, we performed a T-test, ANOVA, Chi-square test, and Pearson correlation analysis.

The results show significant differences in teaching evaluation scores between male and female professors and beauty scores across age groups. However, no significant association was found between gender and tenure status. The analysis also identified a very weak positive correlation between beauty scores and teaching evaluation scores.

Overall, this practical helps us understand how statistical testing can be used to analyse data and make meaningful conclusions.

---

**Tools:** Python | Pandas | SciPy  
**Platform:** Google Colab  
**Project Type:** Data Science Practical – 6
