# Practical 3 – Exploratory Data Analysis Using Python

## 📌 Project Overview

This project focuses on performing basic Exploratory Data Analysis (EDA) on a Professor Evaluation Dataset using Python. The main objective is to understand the dataset, analyse important information, identify patterns, and represent the results using statistical methods and visualisations.

## 📂 Dataset Information

- **Dataset Name:** `evals.csv`
- **Total Records:** 463
- **Total Columns:** 23
- **Data Types:** Numerical and Categorical

The dataset contains information about professors, including:
- Professor ID and Course ID
- Evaluation Scores
- Professor Rank
- Ethnicity and Gender
- Age
- Class Evaluation Percentage
- Student Information
- Professor Appearance Ratings

## 🛠️ Technologies Used

- Python
- Pandas
- Matplotlib
- Google Colab / Jupyter Notebook

## 📦 Libraries Required

```python
import pandas as pd
import matplotlib.pyplot as plt
```

Install the required libraries using:

```bash
pip install pandas matplotlib
```

## 🔍 Analysis Performed

### 1. Loading the Dataset
Loaded the `evals.csv` file using Pandas and displayed the dataset.

### 2. Dataset Information
Used `df.info()` to check:
- Number of rows and columns
- Column names
- Data types
- Missing values

### 3. Descriptive Statistics
Used `df.describe()` to calculate:
- Mean
- Standard Deviation
- Minimum and Maximum
- Quartiles
- Count

### 4. Minority Professors with Tenure
Calculated the percentage of minority professors who are tenured.

**Result:** 40.63%

### 5. Ethnicity vs Professor Rank
Created a cross-tabulation table to compare minority and non-minority professors across different ranks.

### 6. Age Comparison
Calculated the average age and standard deviation of tenured and untenured professors.

| Professor Category | Average Age | Standard Deviation |
|---|---:|---:|
| Tenured | 51.89 | 8.65 |
| Untenured | 44.12 | 9.43 |

### 7. Age Distribution
Created a histogram to understand the age distribution of professors.

### 8. Gender Comparison
Created horizontal and vertical bar charts to compare male and female values using the example counts provided in the code.

### 9. Median Evaluation Score
Calculated the median evaluation score of tenured professors.

**Result:** 4.2

## 📊 Key Findings

- The dataset contains 463 records and 23 columns.
- No missing values were found.
- The average evaluation score is approximately 4.17.
- The average professor age is approximately 48.37 years.
- Around 40.63% of minority professors are tenured.
- Tenured professors are older on average than untenured professors.
- The median evaluation score of tenured professors is 4.2.

## 📈 Visualisations

The project includes:
- Age Distribution Histogram
- Horizontal Gender Bar Chart
- Vertical Gender Bar Chart

These visualisations help make the data easier to understand and compare.

## ▶️ How to Run This Project

1. Clone or download this repository.
2. Open the notebook in Google Colab or Jupyter Notebook.
3. Upload the `evals.csv` dataset.
4. Install the required libraries if needed.
5. Run all code cells.
6. Observe the outputs, tables, and visualisations.

## 📝 Conclusion

This practical demonstrates how Python can be used for basic data analysis. By using Pandas and Matplotlib, we explored professor evaluation data, calculated statistical measures, compared different categories, and created visualisations.

The analysis helps us understand the dataset and identify useful patterns in professor age, gender, ethnicity, tenure status, and evaluation scores.

---

**Tools:** Python | Pandas | Matplotlib  
**Platform:** Google Colab  
**Project Type:** Data Science Practical – 3
