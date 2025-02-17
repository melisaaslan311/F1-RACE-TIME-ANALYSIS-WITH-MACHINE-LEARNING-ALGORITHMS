# 🏎️ Formula 1 Race Time Analysis with Machine Learning

## 📌 Project Overview
This project aims to develop a **predictive model** for Formula 1 race times using **Machine Learning algorithms**. The system can help optimize **race strategies**, **analyze driver performance**, and provide a **competitive advantage** by predicting **race finish times**.

## 🎯 Project Objectives
- 🔹 Create accurate **finish time predictions** using multiple ML models.
- 🔹 Analyze **driver performance** and **constructor efficiency**.
- 🔹 Improve **race strategies** based on predictive analytics.
- 🔹 Support decision-making in **betting markets** with reliable results.

## 🗃️ Dataset Description
https://www.kaggle.com/datasets/rohanrao/formula-1-world-championship-1950-2020
We use multiple datasets merged together for training the models:

| Dataset         | Rows | Columns | Key Features |
|---------------|------|---------|--------------|
| `result.csv` | 26,519 | 19 | Driver & race details, fastest lap times |
| `constructors.csv` | 212 | 5 | Constructor details |
| `races.csv` | 1,125 | 8 | Race-specific information |
| `drivers.csv` | 1,125 | 8 | Driver details |

## 📊 Data Processing Steps
### ✅ Feature Selection
Feature selection is crucial to improving model accuracy and reducing computational cost.  
We applied **Mutual Information** and **Random Forest** methods to select the most significant features:
- **Mutual Information**: Measures **nonlinear dependencies** between variables.
- **Random Forest**: Evaluates the effect of features on model accuracy using **Gini Impurity** or **Entropy**.

### 🔄 Data Preprocessing
- **Min-Max Scaling**: Standardizing numerical features.
- **One-Hot Encoding (`get_dummies`)**: Transforming categorical features into numerical representations.

## ⚡ Model Training with Different Feature Sets
To analyze the impact of feature selection, we trained models using **two different approaches**:
1. **With Important Features (`with_important_features.py`)**:  
   - Used only the **top 4 features** that resulted in the lowest prediction error.
   - Improved computational efficiency and reduced overfitting.
   
2. **With All Features (`with_all_features.py`)**:  
   - Used all available features in the dataset.
   - Provided a comparison to understand the effect of feature selection.

## 🤖 Machine Learning Models Used
We implemented multiple regression algorithms to compare results:

| Algorithm | With Important Features | With All Features |
|-----------|------------------------|------------------|
| 🏆 **Random Forest Regression** | ✅ | ✅ |
| 📈 **Support Vector Regression (SVR)** | ✅ | ✅ |
| 🌳 **Decision Tree Regression** | ✅ | ✅ |
| 🔢 **K-Nearest Neighbors (KNN) Regression** | ✅ | ✅ |
| 🧠 **Artificial Neural Networks (ANNs)** | ✅ | ✅ |

## 🔬 Results & Insights
- **Models trained with only the top 4 features had lower prediction error**, proving the effectiveness of feature selection.
- **Random Forest Regression** performed well in both cases.
- **SVR** effectively captured **nonlinear relationships** in race data.
- **ANNs** produced highly accurate predictions when trained with all features.

## 🛠️ Technologies Used
- **Python** 
