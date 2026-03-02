# 🌲 Forest Cover Type Classification

## 📌 Project Overview

This project focuses on predicting forest cover types using cartographic and environmental features from the Covertype dataset (UCI Machine Learning Repository).

The objective is to build and evaluate multi-class classification models capable of accurately identifying forest cover categories based on geographical attributes.


## 🎯 Problem Statement

Given environmental and cartographic features such as elevation, slope, soil type, and wilderness area, the goal is to classify the forest cover type into one of seven categories.

This is a multi-class classification problem involving large-scale structured tabular data.


## 📊 Dataset Information

- Total Samples: 581,012
- Total Features: 54
- Target Variable: `Cover_Type`
- Number of Classes: 7

The dataset contains:
- Numerical geographic features (Elevation, Slope, Aspect, etc.)
- One-hot encoded Wilderness Areas (4 columns)
- One-hot encoded Soil Types (40 columns)

No missing values were present.


## ⚙️ Methodology

### 1️⃣ Data Preparation
- Sampling for faster experimentation
- Train-test split with stratification
- Label adjustment (1–7 → 0–6 for XGBoost compatibility)

### 2️⃣ Models Implemented
- Random Forest (Baseline)
- XGBoost (Default)
- XGBoost (Hyperparameter Tuned using RandomizedSearchCV)

### 3️⃣ Evaluation Metrics
- Accuracy
- Classification Report (Precision, Recall, F1-score)
- Confusion Matrix
- Cross-Validation Accuracy (CV)


## 📈 Results Summary

| Model | Accuracy |
|--------|----------|
| Random Forest | 90.35% |
| XGBoost (Default) | 84% |
| XGBoost (Tuned) | 89.53% |

After hyperparameter tuning, XGBoost improved significantly from 84% to 89.53%. Random Forest achieved the highest performance at 90.35%.

Both tree-based ensemble methods demonstrated strong effectiveness for this dataset.


## 🔍 Feature Importance

Random Forest and XGBoost feature importance analysis revealed that geographic elevation and distance-based features significantly influence forest cover prediction.


## 🛠️ Technologies Used

- Python
- Pandas
- Scikit-learn
- XGBoost
- Matplotlib
- Seaborn
- Jupyter Notebook


## 🚀 Key Learning Outcomes

- Multi-class classification at scale
- Tree-based ensemble modeling
- Cross-validation techniques
- Hyperparameter tuning using RandomizedSearchCV
- Model comparison and performance analysis
- Confusion matrix interpretation
- Feature importance analysis
