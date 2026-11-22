Data Science Practical 9 – Iris Classification Using K-Nearest Neighbors (KNN)
Overview
This practical implements the K-Nearest Neighbors (KNN) classification algorithm on the Iris dataset (iris.csv). The notebook explores the dataset, scales the features, trains a baseline KNN model (K=5), evaluates it using a confusion matrix and classification report, tunes the optimal K value (K=13) using an error-rate curve, and visualizes the 2D decision boundary.

Objectives
Load and inspect the Iris dataset using Pandas (head(), info(), describe(), and groupby()).

Split the dataset into stratified training (80%) and testing (20%) sets.

Scale numerical features using StandardScaler.

Train a baseline KNeighborsClassifier (K=5, Euclidean distance) and evaluate its accuracy.

Visualize model performance using a Seaborn confusion matrix heatmap and classification_report.

Test K values from 1 to 30 and plot the Error Rate vs K Value curve.

Select the best odd K value (K=13) to improve test accuracy from 93.33% to 96.67%.

Train a 2-feature KNN model (petal_length, petal_width) and plot its decision boundary on the test set.

Tools and Libraries
Python

Google Colab

Pandas – for loading and exploring tabular data.

NumPy – for numerical arrays, meshgrids, and error-rate calculations.

Matplotlib – for plotting the error-rate curve and decision boundary.

Seaborn – for plotting the confusion matrix heatmap.

Scikit-learn – for train-test splitting, feature scaling, KNN modeling, and evaluation metrics.

Dataset
The notebook uses iris.csv, containing 150 rows and 5 columns (with no missing values) across three iris species (setosa, versicolor, virginica):

sepal_length

sepal_width

petal_length

petal_width

species

Make sure iris.csv is available before running the notebook. Upload the CSV file to your Colab session or update the dataset-loading cell with the correct local path or raw GitHub URL.

Important: The notebook currently loads the dataset from /content/iris.csv. Replace this path if your file is stored in a different location before running that cell.

Practical Work
The notebook covers these steps:

Import numpy, pandas, matplotlib, and scikit-learn modules.

Load /content/iris.csv and inspect it with head(), info(), describe(), and groupby("species").mean().

Separate features (X) and target labels (y), then split into 80/20 stratified train and test sets (random_state=42).

Standardize X_train and X_test using StandardScaler.

Train a baseline KNeighborsClassifier(n_neighbors=5, metric="minkowski", p=2) and evaluate it (Accuracy: 0.9333).

Plot the confusion matrix heatmap using Seaborn and print the classification_report.

Loop through K from 1 to 30, record the error rate for each value, and plot Error Rate vs K Value.

Identify the K values achieving the minimum error rate (0.0333), choose the middle odd value (Chosen best K: 13), and retrain final_model (Final Accuracy: 0.9667).

Train knn2 (K=13) on scaled petal_length and petal_width and plot the KNN (K=13) - Test Set Result decision boundary.

Requirements
Install the required packages if they are not already available:

Bash
pip install numpy pandas matplotlib seaborn scikit-learn
Google Colab usually includes all of these libraries by default.

How to Run
Using Google Colab
Open KNN_Practical9.ipynb in Google Colab.

Upload iris.csv to /content/iris.csv (or update the path in the data-loading cell).

Run the notebook cells from top to bottom.

Using Jupyter Notebook locally
Clone or download this repository.

Install the required packages.

Place iris.csv in your working directory and update the file path in the data-loading cell if needed.

Open KNN_Practical9.ipynb in Jupyter Notebook or JupyterLab.

Run the cells from top to bottom.

Repository File
KNN_Practical9.ipynb – Google Colab/Jupyter notebook containing the KNN classification practical.

Author
Dishant Chaudhary

BTech – Computer Science and Engineering (Data Science)
