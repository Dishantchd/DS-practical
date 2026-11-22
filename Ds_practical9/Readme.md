# KNN Classification on Iris Dataset (Practical 9)

A complete end-to-end implementation of the **K-Nearest Neighbors (KNN)** algorithm for multi-class classification using the classic Iris dataset. This notebook demonstrates data exploration, preprocessing, model training, hyperparameter tuning (optimal K selection), evaluation, and decision boundary visualization.

## 📋 Overview

- **Algorithm**: K-Nearest Neighbors Classifier (`sklearn.neighbors.KNeighborsClassifier`)
- **Dataset**: Iris (150 samples, 4 features, 3 classes)
- **Key Steps**:
  1. Exploratory Data Analysis
  2. Feature scaling with `StandardScaler`
  3. Train-test split (80/20, stratified)
  4. KNN model with Euclidean distance
  5. Confusion matrix & classification report
  6. Error rate analysis across K = 1 to 30
  7. Selection of optimal K
  8. Final model evaluation
  9. 2D decision boundary visualization (using petal length & petal width)

## 📊 Dataset

The Iris dataset contains 150 samples of iris flowers with the following features:

| Feature        | Description              |
|----------------|--------------------------|
| `sepal_length` | Sepal length (cm)        |
| `sepal_width`  | Sepal width (cm)         |
| `petal_length` | Petal length (cm)        |
| `petal_width`  | Petal width (cm)         |
| `species`      | Target class (setosa, versicolor, virginica) |

**Class distribution**: 50 samples each of setosa, versicolor, and virginica.

## 🛠️ Requirements

```bash
numpy
pandas
matplotlib
seaborn
scikit-learn


Install with:
pip install numpy pandas matplotlib seaborn scikit-learn


How to Run
Option 1: Google Colab (Recommended)
Open the notebook in [Google Colab](https://colab.research.google.com/).
Upload iris.csv or load it from the provided path.
Run all cells sequentially.
Option 2: Local Jupyter Notebook
Clone this repository.
Place iris.csv in the working directory.
Open the notebook and run all cells.
📈 Key Results
Initial Model (K = 5)
Accuracy: 0.9333
Confusion Matrix:
Text
[[10  0  0]
 [ 0 10  0]
 [ 0  2  8]]
Hyperparameter Tuning (K = 1 to 30)
Error rates were computed for every value of K.
Minimum error rate: ~0.0333
Best K values: Multiple (including 1, 7, 9, 10, 11, 12, 13, 15, 16, 17, 18, 19, 20, 21)
Selected K: 13 (odd value preferred for tie-breaking)
Final Model (K = 13)
Accuracy: 0.9667
2-Feature Visualization
A decision boundary plot was generated using only petal_length and petal_width with the optimal K, clearly showing the separation between the three iris species.

📁 Project Structure
Text
├── KNN_Practical9.ipynb   # Main notebook
├── iris.csv               # Dataset (if provided)
└── README.md              # This file
🔍 Methodology Highlights
Data Preprocessing

Stratified train-test split to maintain class balance
Feature standardization (critical for distance-based algorithms like KNN)
Model Training

Distance metric: Minkowski with p=2 (Euclidean)
Hyperparameter search over a wide range of K values
Evaluation

Confusion matrix heatmap
Classification report (precision, recall, F1-score)
Error rate vs K plot to identify the elbow / optimal region
Visualization

Decision regions for the two most discriminative features (petal length & width)
📝 Notes
The optimal K was chosen as an odd number among the best-performing values to avoid ties in majority voting.
Using only petal features still yields strong class separation, confirming their high discriminative power.
Scaling is essential — without it, features with larger ranges would dominate the distance calculations.
👤 Author
Practical 9 – Machine Learning Lab
KNN Classifier Implementation
