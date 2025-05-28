# Milling Machine Tool Wear Failure Prediction

## 👤 Author

| Name            | Role              | LinkedIn                                      |
|-----------------|-------------------|-----------------------------------------------|
| Jason Emmanuel  | Data Scientisst | [linkedin.com/in/jasoneml](https://www.linkedin.com/in/jasoneml/) |

---

## 📋 Overview

This project aims to predict tool wear failures in milling machines using machine learning techniques. Tool wear is a significant factor in manufacturing that can lead to poor product quality and unplanned downtime. By leveraging historical sensor data and predictive modeling, we can proactively identify potential failures and perform timely maintenance.

![image](https://github.com/user-attachments/assets/4efe4d15-8896-4ed4-82bc-f55a18474fcb)

---

## 📊 Dataset

The dataset used is `ai4i2020.csv`, which includes readings from various sensors in a milling machine. Features include:
- Air temperature [K]
- Process temperature [K]
- Rotational speed [rpm]
- Torque [Nm]
- Tool wear [min]
- Machine failure (target)
- Failure types: TWF, HDF, PWF, OSF, RNF

---

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

---

## 📊 Results

![image](https://github.com/user-attachments/assets/2c397aac-5180-4a07-bb1a-2b57ed090471)

This confusion matrix shows the performance of a binary classification model. The model correctly predicted 1,894 instances of class 0 (true negatives) and 45 instances of class 1 (true positives). It incorrectly classified 45 instances of class 0 as class 1 (false positives) and 16 instances of class 1 as class 0 (false negatives). Overall, the model demonstrates strong accuracy for class 0 but relatively lower precision and recall for class 1, indicating potential class imbalance or difficulty in identifying class 1 correctly.

![image](https://github.com/user-attachments/assets/e68410d9-4c79-4a53-a675-e2660a54f61f)

This classification report visualizes the performance metrics for a binary classifier distinguishing between "No Failure" and "Failure" classes. The model performs very well on the "No Failure" class, with high precision (0.99), recall (0.98), and F1-score (0.98). However, for the "Failure" class, the performance drops significantly, particularly in precision (0.50), although recall is relatively better (0.74), leading to a moderate F1-score of 0.60. The overall accuracy is high at 0.97, but the macro average (0.75 precision, 0.86 recall, 0.79 F1-score) reflects the performance imbalance between the classes, indicating that the model is biased toward the majority class.

![image](https://github.com/user-attachments/assets/81ec147b-024e-40b1-aa31-bdd374a95fb3)

The ROC curve shows that the model performs very well, with an AUC (Area Under the Curve) of 0.97. This means the model is highly effective at distinguishing between the two classes, with excellent accuracy and low error rates.

![image](https://github.com/user-attachments/assets/c11ac2f5-5b1b-4e72-90bc-545cc8bd016a)

This bar chart shows the importance of different features in a predictive model. The most influential features are Rotational speed [rpm] and Torque [Nm], each contributing the most to the model's predictions. Tool wear [min] also has a significant impact, while Air temperature [K] and Process temperature [K] have the least importance. This suggests that mechanical factors like speed, torque, and wear are more critical in determining the target outcome than temperature-related features in this context.

![image](https://github.com/user-attachments/assets/2493faf0-dac1-4dd9-83db-21dd8a7ee313)

This image is a visualization of a Random Forest model, specifically showing a single decision tree from the ensemble. The tree is highly complex, with many levels and branches, indicating deep and intricate decision rules learned from the dataset. Each node represents a decision based on a feature threshold, and the color of each node indicates the class it is biased toward—typically orange for one class and blue for another. The depth and spread of the tree suggest a high model complexity, potentially fitting a detailed pattern in the training data. This visualization helps in understanding how individual trees contribute to the ensemble's decision-making process in the Random Forest algorithm used for tool wear failure prediction.

---

### 🧰 Tools and Libraries Used

| Library/Tool     | Purpose                                                       |
|------------------|---------------------------------------------------------------|
| `pandas`         | Data loading, manipulation, and analysis                      |
| `numpy`          | Numerical computations and array handling                     |
| `matplotlib`     | Data visualization (e.g., plotting graphs)                    |
| `seaborn`        | Enhanced statistical data visualization (e.g., heatmaps)      |
| `scikit-learn`   | Model building, evaluation, hyperparameter tuning, and SMOTE  |
| `imblearn`       | Handling imbalanced datasets using techniques like SMOTE      |
| `joblib`         | Model serialization and saving                                |

---

## 💻 Installation

### 📦 Requirements

Install the required Python packages with:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn imbalanced-learn graphviz
```
