# Practical 10: Principal Component Analysis (PCA) – Wine Dataset

## 📌 Project Overview

This practical demonstrates **Principal Component Analysis (PCA)** using the Wine Recognition Dataset.

PCA is a dimensionality reduction technique used to transform a dataset with multiple features into a smaller set of principal components while retaining as much information (variance) as possible.

The main objective is to analyse the chemical properties of wine and visualize the separation between three different wine classes.

## 🎯 Objectives

1. Display basic statistical information using `describe()`.
2. Create boxplots based on output labels/classes.
3. Create a scatterplot using two variables.
4. Calculate and visualize the covariance matrix.
5. Perform data scaling using StandardScaler.
6. Apply PCA to reduce dimensions and visualize better class separation.

## 📊 Dataset Description

The Wine Recognition Dataset contains chemical analysis results of wines belonging to three different classes.

- **Total Samples:** 178
- **Total Features:** 13
- **Target Classes:** 3 (Class 1, Class 2, Class 3)

### Features

The dataset contains the following chemical properties:

- Alcohol
- Malic acid
- Ash
- Alcalinity of ash
- Magnesium
- Total phenols
- Flavanoids
- Nonflavanoid phenols
- Proanthocyanins
- Color intensity
- Hue
- OD280/OD315 of diluted wines
- Proline

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Google Colab

## 📚 Libraries Used

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

from sklearn.preprocessing import StandardScaler
from sklearn.decomposition import PCA
```

## 🔍 Practical Implementation

### 1. Basic Statistical Analysis

Used `df.describe()` to display statistical information such as:

- Count
- Mean
- Standard Deviation
- Minimum
- Maximum
- 25%, 50%, and 75% Percentiles

### 2. Boxplot by Wine Classes

Created boxplots for:

- Alcohol
- Malic Acid
- Color Intensity

These plots help compare the distribution of chemical properties across the three wine classes and identify possible outliers.

### 3. Scatterplot

Created a scatterplot using:

- X-axis: Alcohol
- Y-axis: Color Intensity
- Hue: Wine Class

This visualization helps identify relationships between alcohol content and color intensity across different wine classes.

### 4. Covariance Matrix

Calculated the covariance matrix using:

```python
X = df.drop('class', axis=1)
cov_matrix = X.cov()
```

Visualized the covariance matrix using a Seaborn heatmap to understand relationships between numerical features.

### 5. Data Scaling

Applied StandardScaler to standardize the features.

```python
X = df.drop('class', axis=1)
y = df['class']

scaler = StandardScaler()
X_scaled = scaler.fit_transform(X)
```

StandardScaler transforms the features so that they have approximately:

- Mean = 0
- Standard Deviation = 1

Scaling is important because PCA is affected by differences in feature scales.

### 6. Principal Component Analysis (PCA)

Applied PCA to reduce the original 13 features into 2 principal components.

```python
pca = PCA(n_components=2)

X_pca = pca.fit_transform(X_scaled)
```

Created a DataFrame containing PC1, PC2, and the original wine class labels.

The explained variance ratio obtained was:

- **PC1:** 36.20%
- **PC2:** 19.21%
- **Total Variance Explained:** 55.41%

The final PCA scatterplot visualizes the separation between the three wine classes using two principal components.

## 📈 Results and Observations

- The dataset contains 178 wine samples and 13 chemical features.
- The dataset has three different wine classes.
- Boxplots show variations in chemical properties among the classes.
- The scatterplot shows differences between wine classes based on alcohol and color intensity.
- The covariance matrix helps identify relationships between chemical features.
- StandardScaler brings all features to a comparable scale.
- PCA reduces the dimensionality from 13 features to 2 principal components.
- The first two principal components retain approximately 55.41% of the total variance.
- The PCA visualization shows better separation between the three wine classes.

## 🧠 What is PCA?

Principal Component Analysis (PCA) is a dimensionality reduction technique used in machine learning and data analysis.

It converts a dataset with many correlated features into a smaller number of uncorrelated variables called principal components.

**Advantages of PCA:**

- Reduces dataset dimensionality.
- Helps visualize high-dimensional data.
- Removes redundancy caused by correlated features.
- Can improve computational efficiency.
- Helps identify patterns in data.

## ▶️ How to Run This Project

1. Clone this repository:

```bash
git clone https://github.com/your-username/your-repository-name.git
```

2. Navigate to the project folder:

```bash
cd your-repository-name
```

3. Install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

4. Open the notebook in Google Colab or Jupyter Notebook.

5. Upload the Wine dataset CSV file (`Wine dataset.csv`).

6. Run all the cells to perform statistical analysis, visualization, scaling, and PCA.

## 📁 Project Structure

```text
Practical-10-PCA/
│
├── README.md
├── Practical10_PCA.ipynb
└── Wine dataset.csv
```

## 🏁 Conclusion

In this practical, Principal Component Analysis (PCA) was successfully applied to the Wine Recognition Dataset.

The original 13-dimensional dataset was reduced to 2 principal components, retaining approximately 55.41% of the total variance.

The final visualization demonstrates how PCA can help identify patterns and improve the visual separation of different wine classes.

---

**Practical No.:** 10  
**Topic:** Principal Component Analysis (PCA)  
**Dataset:** Wine Recognition Dataset  
**Environment:** Google Colab / Python
