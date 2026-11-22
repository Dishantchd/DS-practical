# Practical 5 – Probability and Hypothesis Testing Using Python

## 📌 Project Overview

This practical focuses on Probability and Hypothesis Testing using Python. The analysis is performed on the Teaching Ratings Dataset to understand evaluation score probabilities and perform a two-tailed Z-test.

The main objective is to calculate probabilities, understand normal distribution, and test whether two average scores are significantly different.

## 📂 Dataset Information

- **Dataset Name:** `TeachingRatings.csv`
- **Total Observations:** 463
- **Total Columns:** 13

The dataset contains information about professors, including:
- Professor Age
- Gender
- Minority Status
- Teaching Evaluation Scores
- Course Division
- Tenure Status
- Beauty Ratings
- Number of Students

## 🛠️ Technologies Used

- Python
- Pandas
- SciPy
- Math
- Google Colab / Jupyter Notebook

## 📦 Libraries Required

```python
import pandas as pd
from scipy import stats
import math
```

Install the required libraries using:

```bash
pip install pandas scipy
```

## 🔍 Analysis Performed

### 1. Loading the Dataset

Loaded the `TeachingRatings.csv` file using Pandas to access and analyse the professor evaluation data.

### 2. Calculating Mean and Standard Deviation

Calculated the average evaluation score and sample standard deviation.

**Results:**
- Mean Evaluation Score: 3.9983
- Standard Deviation: 0.5549

These values are used for calculating probabilities based on the normal distribution.

### 3. Q1 – Probability of Evaluation Score Greater Than 4.5

Calculated the probability that a professor receives an evaluation score greater than 4.5.

Two methods were used:

- **Theoretical Probability:** Calculated using the normal distribution.
- **Actual Probability:** Calculated directly from the dataset.

**Results:**
- Theoretical Probability: 18.29%
- Actual Probability: 17.06%
- Z-score: 0.9042

**Finding:** Approximately 17.06% of the actual evaluation records have scores greater than 4.5. The theoretical estimate is slightly higher at 18.29%.

### 4. Q2 – Probability of Evaluation Score Between 3.5 and 4.2

Calculated the probability that an evaluation score falls between 3.5 and 4.2.

Two methods were used to compare the results.

**Results:**
- Theoretical Probability: 45.73%
- Actual Probability: 35.42%
- Lower Z-score: -0.8980
- Upper Z-score: 0.3636

**Finding:** According to the actual dataset, approximately 35.42% of evaluation scores fall between 3.5 and 4.2. The normal distribution estimates this probability at 45.73%.

### 5. Q3 – Two-Tailed Z-Test (Basketball Scores)

Performed a two-tailed Z-test to compare a sample mean with a historical population mean.

**Given Values:**

- Historical Population Mean (μ): 12
- Population Standard Deviation (σ): 5.5
- Sample Size (n): 36
- Sample Mean: 10.7
- Significance Level (α): 0.05

**Results:**

- Standard Error: 0.9167
- Z-statistic: -1.4182
- P-value: 0.1561
- Critical Z-value: ±1.9600

**Hypothesis:**

- Null Hypothesis (H0): There is no significant difference between the sample mean and historical population mean.
- Alternative Hypothesis (H1): There is a significant difference between the sample mean and historical population mean.

**Decision:** Fail to Reject H0.

**Finding:** Since the p-value (0.1561) is greater than the significance level (0.05), there is not enough statistical evidence to conclude that the sample mean is significantly different from the historical population mean.

## 📊 Key Findings

- The average teaching evaluation score is approximately 4.00.
- The sample standard deviation is 0.5549.
- Around 17.06% of actual evaluation scores are greater than 4.5.
- Around 35.42% of actual evaluation scores fall between 3.5 and 4.2.
- The theoretical probabilities are different from the actual probabilities.
- The two-tailed Z-test shows no statistically significant difference at the 5% significance level.

## ▶️ How to Run This Project

1. Clone or download this GitHub repository.
2. Open the notebook in Google Colab or Jupyter Notebook.
3. Upload the `TeachingRatings.csv` dataset.
4. Install the required Python libraries.
5. Run all code cells.
6. Observe the probability calculations and hypothesis testing results.

## 📝 Conclusion

This practical demonstrates how Python can be used for probability calculations and hypothesis testing.

Using Pandas and SciPy, we calculated the mean, standard deviation, theoretical probability, and actual probability of teaching evaluation scores.

We also performed a two-tailed Z-test to compare a sample mean with a historical population mean. The test result showed that there was no statistically significant difference at the 5% significance level.

Overall, this practical helps us understand probability, normal distribution, Z-scores, p-values, and hypothesis testing using real-world data.

---

**Tools:** Python | Pandas | SciPy | Math  
**Platform:** Google Colab  
**Project Type:** Data Science Practical – 5
