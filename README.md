# Client Term Deposit Subscription Prediction

This project focuses on predicting whether a bank customer will subscribe to a term deposit based on historical marketing campaign data. By utilizing machine learning classification models, the goal is to help financial institutions optimize their marketing strategies and improve conversion rates.

## 📋 Project Overview
Telemarketing campaigns are often resource-intensive. This project develops a predictive system to estimate the probability of a customer subscribing to a term deposit. By identifying high-value leads, banks can reduce operational costs and target customers more effectively.

## 📊 Dataset Description
The analysis uses the **Bank Marketing Dataset**, which contains 41,188 records and 21 features:
- **Target Variable (y):** Binary (1 for 'Yes', 0 for 'No').
- **Quantitative Features:** Age, campaign contacts, days since last contact (pdays), and economic indicators (euribor3m, consumer price index, etc.).
- **Categorical Features:** Job, marital status, education, credit default, housing, and loans.

## 🛠️ Tech Stack
- **Languages:** Python
- **Libraries:** Pandas, NumPy, Scikit-learn, TensorFlow/Keras, Matplotlib, Seaborn

## ⚙️ Methodology
### 1. Data Preprocessing
- **Outlier Treatment:** Handled using the whisker method.
- **Feature Engineering:** Dropped the `duration` column to prevent data leakage and ensure realistic model performance.
- **Encoding:** Applied Label Encoding for binary features and One-Hot Encoding for categorical variables.
- **Scaling:** Features were standardized using `StandardScaler` to ensure uniform influence.
- **Data Splitting:** 80% Training and 20% Testing.

### 2. Model Training
Three classification models were trained and compared:
- **Logistic Regression:** Designed for binary classification and efficient with tabular data.
- **Decision Tree Classifier:** Captures non-linear relationships and provides high interpretability.
- **Neural Network (MLP):** Capable of learning complex feature combinations and non-linear patterns.

## 📈 Results and Comparison
All models achieved approximately 90% accuracy. The **Decision Tree Classifier** emerged as the top performer for this specific task.

| Model | Accuracy | ROC-AUC |
|-------|----------|---------|
| **Decision Tree** | **89.98%** | **0.8002** |
| Logistic Regression | 89.79% | 0.7999 |
| Neural Network | 89.82% | 0.7724 |

*Note: Models still struggle with the minority class ('Yes') due to class imbalance (11.27% vs 88.73%).*


