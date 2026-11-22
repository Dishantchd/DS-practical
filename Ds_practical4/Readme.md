# Practical 4 – Teaching Ratings Data Analysis Using Python

## 📌 Project Overview

This project focuses on analysing a Teaching Ratings Dataset using Python. The main objective is to explore professor evaluation scores and understand how factors such as age, gender, tenure, beauty, and course division relate to teaching evaluations.

The project uses Pandas for data analysis and Matplotlib for data visualisation.

## 📂 Dataset Information

- **Dataset Name:** `TeachingRatings.csv`
- **Total Observations:** 463
- **Unique Instructors:** 94
- **Total Columns:** 13

### Dataset Features

The dataset contains the following information:

- `minority` – Indicates whether the professor belongs to a minority group.
- `age` – Age of the professor.
- `gender` – Gender of the professor.
- `credits` – Course credit category.
- `beauty` – Professor beauty rating.
- `eval` – Teaching evaluation score.
- `division` – Course division (Lower or Upper).
- `native` – Indicates whether the professor is a native English speaker.
- `tenure` – Tenure status of the professor.
- `students` – Number of students who evaluated the professor.
- `allstudents` – Total number of students in the class.
- `prof` – Professor ID.

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

Loaded the `TeachingRatings.csv` file using Pandas and displayed the dataset.

### 2. Removing Duplicate Professors

Used `drop_duplicates()` to remove repeated professor records based on the `prof` column.

- Original observations: 463
- Unique instructors: 94

This helps analyse each professor only once when studying instructor-level information.

### 3. Descriptive Statistical Analysis

Used `df_unique.describe()` to calculate statistical measures such as:

- Mean
- Standard Deviation
- Minimum and Maximum
- Median
- Quartiles

### 4. Comparing Average Teaching Evaluation by Division

Created a bar chart to compare the average teaching evaluation scores of lower and upper division courses.

**Results:**

- Lower Division: 4.087
- Upper Division: 3.953

**Finding:** Lower-division instructors receive slightly higher average evaluation scores than upper-division instructors.

### 5. Age vs Teaching Evaluation

Created a scatter plot to understand the relationship between professor age and teaching evaluation scores.

**Finding:** The scatter plot shows no strong relationship between age and teaching evaluation scores.

### 6. Age vs Evaluation by Gender

Created a scatter plot to compare male and female professors based on age and evaluation scores.

**Finding:** Male and female professors show similar patterns in teaching evaluation scores. No strong age effect is observed.

### 7. Age vs Evaluation by Gender and Tenure

Created a scatter plot by grouping professors based on gender and tenure status.

The chart displays four groups:

- Female – No Tenure
- Female – Tenure
- Male – No Tenure
- Male – Tenure

**Finding:** Age remains a weak predictor of teaching evaluation scores across all four groups.

## 📊 Key Findings

- The dataset contains 463 observations and 94 unique instructors.
- The average age across all observations is approximately 48.37 years.
- The average age of unique instructors is approximately 47.55 years.
- Lower-division instructors have slightly higher average evaluation scores than upper-division instructors.
- The relationship between professor age and teaching evaluation scores is weak.
- Male and female professors show similar evaluation patterns.
- Age does not appear to be a strong predictor of teaching evaluation scores in this dataset.

## 📈 Visualisations

The project includes the following charts:

1. Average Teaching Evaluation by Division – Bar Chart.
2. Age vs Teaching Evaluation – Scatter Plot.
3. Age vs Evaluation by Gender – Scatter Plot.
4. Age vs Evaluation by Gender and Tenure – Grouped Scatter Plot.

These visualisations help identify patterns and compare teaching evaluation scores across different professor groups.

## ▶️ How to Run This Project

1. Clone or download this repository.
2. Open the notebook using Google Colab or Jupyter Notebook.
3. Upload the `TeachingRatings.csv` dataset.
4. Install the required Python libraries.
5. Run all code cells.
6. Observe the statistical outputs and visualisations.

## 📝 Conclusion

This practical demonstrates how Python can be used to analyse teaching evaluation data. Using Pandas and Matplotlib, we explored professor information, removed duplicate records, calculated descriptive statistics, and created different visualisations.

The analysis shows that lower-division instructors receive slightly higher average evaluation scores. It also indicates that professor age has a weak relationship with teaching evaluation scores, while male and female professors show similar patterns.

Overall, this practical helps us understand how data analysis and visualisation can be used to explore teaching evaluation patterns.

---

**Tools:** Python | Pandas | Matplotlib  
**Platform:** Google Colab  
**Project Type:** Data Science Practical – 4
