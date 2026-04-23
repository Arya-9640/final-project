Cardiovascular Disease Prediction Using Machine Learning
Overview

This project investigates whether supervised machine learning models can predict the presence of cardiovascular disease using structured clinical and lifestyle data. The study compares three models: Random Forest, Support Vector Machine (SVM), and XGBoost. The work includes data cleaning, feature engineering, exploratory data analysis, model training, hyperparameter tuning, and evaluation using multiple performance metrics.

Research Question

Can machine learning models accurately predict the presence of cardiovascular disease using structured clinical data, and which model performs best for this task?

Objectives
Clean and preprocess the cardiovascular dataset
Perform exploratory data analysis
Train Random Forest, SVM, and XGBoost models
Tune the models using hyperparameter optimisation
Compare the models using multiple evaluation metrics
Dataset

This project uses the Enhanced Cardiovascular Disease Dataset with Data Augmentation from IEEE DataPort.

Dataset link:
https://ieee-dataport.org/documents/enhanced-cardiovascular-disease-dataset-data-augmentation-0

The dataset includes variables such as:

age
gender
height
weight
systolic blood pressure (ap_hi)
diastolic blood pressure (ap_lo)
cholesterol
glucose
smoking
alcohol intake
physical activity
BMI
target variable: cardio
Tools and Libraries

The project was implemented in Python using:

pandas
numpy
matplotlib
seaborn
scikit-learn
xgboost
Project Workflow
Load the dataset
Remove the id column
Convert age from days to years
Filter unrealistic blood pressure, height, and weight values
Create BMI as a derived feature
Split data into training and testing sets
Scale numerical features for SVM
Train baseline Random Forest, SVM, and XGBoost models
Tune the models using RandomizedSearchCV
Evaluate the models using accuracy, precision, recall, F1-score, confusion matrix, ROC curve, and AUC
Models Used
Random Forest

An ensemble classifier that combines multiple decision trees using majority voting.

Support Vector Machine

A margin-based classifier using the RBF kernel for non-linear separation.

XGBoost

A gradient boosting classifier that builds trees sequentially to reduce previous errors.

Evaluation Metrics

The following metrics were used:

Accuracy
Precision
Recall
F1-score
Confusion Matrix
ROC Curve
AUC
Main Results
Random Forest Accuracy: 70.36%
SVM Accuracy: 72.72%
XGBoost Accuracy: 72.68%
Best tuned ROC-AUC
Random Forest: 0.8025
SVM: 0.7954
XGBoost: 0.8037
Best Model Interpretation
SVM achieved the highest held-out test accuracy
XGBoost achieved the best cross-validated ROC-AUC
How to Run
1. Install required libraries
pip install pandas numpy matplotlib seaborn scikit-learn xgboost
2. Start Jupyter Notebook
jupyter notebook
3. Open the notebook

Open the project notebook file and run the cells in order.

4. Dataset path

Make sure the dataset CSV file is in the correct folder and that the file path in the code matches your local machine.

Repository Structure
├── data/
│   └── cardio_train.csv
├── notebooks/
│   └── cardiovascular_disease_prediction.ipynb
├── images/
│   ├── eda_plots/
│   ├── confusion_matrices/
│   └── roc_curves/
├── report/
│   └── final_report.pdf
├── README.md
└── requirements.txt
