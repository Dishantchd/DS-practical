# Decision Tree Classification Using Python

## 1. Project Overview

This project uses a **Decision Tree Classifier** to predict whether a person has diabetes or not. The model is trained using the Pima Indians Diabetes Dataset.

The practical also compares two decision tree methods, **Entropy and Gini**, and evaluates the model using accuracy, a confusion matrix, and a classification report.

## 2. Dataset Information

- **Dataset:** Pima Indians Diabetes Dataset
- **Total Records:** 768
- **Total Columns:** 9
- **Target Column:** `Outcome`
- **0:** No Diabetes
- **1:** Diabetes

### Features Used

1. Pregnancies
2. Glucose
3. BloodPressure
4. SkinThickness
5. Insulin
6. BMI
7. DiabetesPedigreeFunction
8. Age

## 3. Technologies Used

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Scikit-learn

## 4. Libraries Used

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt

from sklearn.model_selection import train_test_split
from sklearn.tree import DecisionTreeClassifier, plot_tree, export_text
from sklearn.metrics import accuracy_score, confusion_matrix, classification_report
from sklearn.feature_selection import mutual_info_classif
```

## 5. Data Loading and Inspection

The dataset was loaded from an online source and inspected using basic Pandas functions.

**Output:**
- Total records: 768
- Total columns: 9
- No Diabetes: 500
- Diabetes: 268

**Interpretation:** The dataset contains 768 records. Out of these, 500 people are classified as non-diabetic and 268 people are classified as diabetic.

## 6. Data Cleaning

Zero values in Glucose, BloodPressure, SkinThickness, Insulin, and BMI were replaced with missing values. These missing values were then filled using the median of each column.

**Interpretation:** This step helps handle invalid zero values and prepares the dataset for model training.

## 7. Feature Selection

The target variable was separated from the independent features.

- **Features (X):** Health-related information such as glucose, BMI, age, and insulin.
- **Target (y):** Outcome, which represents whether a person has diabetes or not.

## 8. Splitting the Dataset

The dataset was divided into training and testing sets.

- Training records: 614
- Testing records: 154
- Test size: 20%

**Interpretation:** The model uses 614 records for learning and 154 records for testing its prediction performance.

## 9. Feature Importance Checks

Mutual Information and Correlation were used to understand which features are more related to the diabetes outcome.

**Important observations:**
- Glucose has the highest mutual information score (0.1177).
- BMI has the second-highest score (0.0887).
- Glucose also has the strongest correlation with Outcome (0.5123).

**Interpretation:** Glucose appears to be the most informative feature for predicting diabetes in this dataset.

## 10. Decision Tree Using Entropy and Gini

Two decision tree criteria were compared:
- **Entropy:** Measures uncertainty in the data.
- **Gini:** Measures how mixed the classes are.

Different maximum tree depths were tested to compare training and testing accuracy.

**Best results from the comparison:**

| Criterion | Maximum Depth | Training Accuracy | Testing Accuracy |
|---|---:|---:|---:|
| Entropy | 4 | 77.7% | 79.2% |
| Gini | 4 | 79.5% | 78.6% |

**Interpretation:** Entropy with a maximum depth of 4 achieved the highest testing accuracy of 79.2% among the tested settings.

The practical then selected an Entropy-based tree with a maximum depth of 3 for further evaluation.

## 11. Model Evaluation

The selected model was evaluated using test data.

**Results:**
- Training Accuracy: 76.7%
- Testing Accuracy: 68.8%

**Confusion Matrix:**

```text
[[92  8]
 [40 14]]
```

**Interpretation:**
- 92 non-diabetic cases were correctly predicted.
- 8 non-diabetic cases were incorrectly predicted as diabetic.
- 40 diabetic cases were incorrectly predicted as non-diabetic.
- 14 diabetic cases were correctly predicted.

**Classification Report:**

| Class | Precision | Recall | F1-Score |
|---|---:|---:|---:|
| No Diabetes | 0.70 | 0.92 | 0.79 |
| Diabetes | 0.64 | 0.26 | 0.37 |

**Interpretation:** The model performs better at identifying people without diabetes. However, it misses many diabetic cases, so its ability to detect diabetes needs improvement.

## 12. Decision Tree Visualization

The decision tree was displayed using `plot_tree()` and `export_text()`.

**Interpretation:** The visualization shows how the model makes predictions by checking conditions on features such as Glucose, BMI, and Insulin. Each branch represents a decision, and the final leaf represents the predicted class.

## 13. Feature Importance

A feature importance graph was created to identify which features contribute most to the decision tree's predictions.

**Interpretation:** Feature importance helps us understand which health-related variables the model uses most when making its predictions.

## 14. Entropy, Information Gain, and Gini

The practical calculated Entropy, Information Gain, and Gini Reduction to understand how the decision tree selects its first split.

**Results:**
- Parent Entropy: 0.9328
- Parent Gini: 0.4541
- Root Feature: Glucose
- Best Root Threshold: 154.50

**Interpretation:** Glucose was selected as the root feature because splitting the data at a Glucose value of 154.50 provided the highest Information Gain among the tested features.

## 15. Key Findings

1. The dataset contains 768 records and 9 columns.
2. Glucose is the most informative feature according to the Mutual Information results.
3. Entropy with a maximum depth of 4 achieved the highest test accuracy of 79.2% in the comparison.
4. The selected Entropy model with depth 3 achieved 68.8% test accuracy.
5. The model identifies non-diabetic cases better than diabetic cases.
6. Glucose was selected as the root feature of the decision tree.

## 16. Conclusion

In this practical, a Decision Tree Classifier was used to predict diabetes using health-related information. Entropy and Gini methods were compared, and different tree depths were tested.

The comparison showed that Entropy with a maximum depth of 4 achieved 79.2% testing accuracy. However, the selected depth-3 model achieved 68.8% testing accuracy and had difficulty identifying diabetic cases.

Overall, this practical demonstrates how decision trees can be used for classification and how model performance can be evaluated using different metrics.

**Note:** This is an educational machine learning project, not a medical diagnostic tool.
