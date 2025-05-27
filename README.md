# ⚙️ Milling Machine Tool Wear Failure Prediction

## 📋 Overview

This project aims to predict tool wear failures in milling machines using machine learning techniques. Tool wear is a significant factor in manufacturing that can lead to poor product quality and unplanned downtime. By leveraging historical sensor data and predictive modeling, we can proactively identify potential failures and perform timely maintenance.

## 📊 Dataset

The dataset used is `ai4i2020.csv`, which includes readings from various sensors in a milling machine. Features include:
- Air temperature [K]
- Process temperature [K]
- Rotational speed [rpm]
- Torque [Nm]
- Tool wear [min]
- Machine failure (target)
- Failure types: TWF, HDF, PWF, OSF, RNF

## 🎯 Project Objectives

1. Import Libraries & Load Data  
2. Select Features & Target  
3. Train-Test Data Split  
4. Data Preprocessing (Scaling and SMOTE)  
5. Model Building (Random Forest)  
6. Hyperparameter Tuning (GridSearchCV)  
7. Model Evaluation (confusion matrix, classification report, ROC-AUC)  
8. Feature Importance Visualization  
9. Model Testing and Sample Prediction  
10. Visualize Decision Tree

## 💻 Installation

### 📦 Requirements

Install the required Python packages with:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn graphviz
```
