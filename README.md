# Predictive Analytics for Urban Transit: Bus Delay Prediction System

A machine learning-based predictive analytics system for urban transit delay forecasting and delay classification. The project uses historical transit features such as traffic density, weather conditions, distance, and temporal attributes to predict bus delays and identify potentially delayed trips.

Developed as part of the **Mathematical Models for Machine Learning (MML)** coursework.

---

## Project Overview

Urban transit systems are affected by factors such as traffic congestion, weather conditions, peak-hour demand, and route characteristics. Accurate delay prediction can help improve scheduling, passenger information systems, and operational planning.

This project addresses two predictive tasks:

### 1. Delay Duration Prediction (Regression)

Predict the actual delay duration of a bus trip in minutes.

### 2. Delay Classification (Binary Classification)

Predict whether a bus trip will be delayed or not.

The project evaluates and compares multiple machine learning models and identifies the best-performing approach based on quantitative performance metrics.

---

## Tech Stack

* Python
* Pandas
* NumPy
* Scikit-learn
* XGBoost
* Matplotlib
* Seaborn
* Jupyter Notebook

---

## Models Evaluated

### Regression Models

* Linear Regression
* Decision Tree Regressor
* XGBoost Regressor

### Classification Models

* Thresholded Linear Regression
* Decision Tree Classifier
* XGBoost Classifier

---

## Results

### Delay Duration Prediction

| Model             | MSE  | RMSE |
| ----------------- | ---- | ---- |
| Linear Regression | 6.93 | 2.63 |
| Decision Tree     | 8.61 | 2.93 |
| XGBoost           | 4.71 | 2.17 |

### Delay Classification

| Model                           | Accuracy | Precision | Recall | F1 Score |
| ------------------------------- | -------- | --------- | ------ | -------- |
| Linear Regression (Thresholded) | 94.0%    | 96.7%     | 96.7%  | 96.7%    |
| Decision Tree                   | 93.0%    | 95.9%     | 96.6%  | 96.2%    |
| XGBoost                         | 94.83%   | 96.0%     | 98.55% | 97.2%    |

### Key Finding

XGBoost achieved the best overall performance for both regression and classification tasks, delivering the lowest prediction error and highest classification accuracy.

---

## Dataset

A synthetic dataset containing **3,000 urban transit records** was generated to simulate realistic bus operations.

### Features

* Distance to Stop
* Traffic Density
* Weather Condition
* Hour of Day
* Day of Week
* Peak Hour Indicator
* Weekend Indicator

### Targets

* Actual Delay (minutes)
* Delay Status (Delayed / Not Delayed)

Feature engineering was used to derive temporal indicators such as peak-hour and weekend flags.

---

## Project Workflow

```text
Data Generation
       ↓
Feature Engineering
       ↓
Train-Test Split
       ↓
Model Training
       ↓
Regression Evaluation
       ↓
Classification Evaluation
       ↓
Model Comparison
       ↓
Performance Visualization
```

---

## Repository Structure

```text
urban-transit-analytics/
│
├── BUS_TRACKING_SYSTEM.ipynb
├── Report.pdf
├── requirements.txt
└── README.md
```

---

## Visualizations

The project includes:

* Correlation Heatmap
* Regression Performance Comparison
* Classification Performance Comparison
* ROC Curve
* Confusion Matrix
* Actual vs Predicted Delay Analysis

---

## Key Learnings

* Feature Engineering
* Regression Modeling
* Binary Classification
* XGBoost Implementation
* Model Evaluation and Comparison
* ROC-AUC Analysis
* Confusion Matrix Interpretation
* Predictive Analytics for Transportation Systems

---

## Limitations

* Dataset is synthetic and may not fully capture real-world transit behavior.
* No real-time GPS integration.
* No web deployment or production inference pipeline.
* Results may differ when evaluated on real operational transit data.

---

## Future Improvements

* Integration with real-world GPS and transit feeds
* Real-time prediction API using FastAPI
* Cloud deployment for scalable inference
* Additional ensemble models such as Random Forest, LightGBM, and CatBoost
* Model explainability using SHAP

---

## Author

Annu Mary Mahesh
