# Client Term Deposit Subscription Prediction

This project focuses on predicting whether a bank customer will subscribe to a term deposit based on historical marketing campaign data. By utilizing machine learning classification models, the goal is to help financial institutions optimize their marketing strategies and improve conversion rates.

## 📋 Project Overview
Telemarketing campaigns are often resource-intensive. This project develops a predictive system to estimate the probability of a customer subscribing to a term deposit. [cite_start]By identifying high-value leads, banks can reduce operational costs and target customers more effectively[cite: 8, 9, 11].

## 📊 Dataset Description
[cite_start]The analysis uses the **Bank Marketing Dataset**, which contains 41,188 records and 21 features[cite: 16, 18]:
- [cite_start]**Target Variable (y):** Binary (1 for 'Yes', 0 for 'No')[cite: 17].
- [cite_start]**Quantitative Features:** Age, campaign contacts, days since last contact (pdays), and economic indicators (euribor3m, consumer price index, etc.)[cite: 18].
- [cite_start]**Categorical Features:** Job, marital status, education, credit default, housing, and loans[cite: 19].

## 🛠️ Tech Stack
- **Languages:** Python
- **Libraries:** Pandas, NumPy, Scikit-learn, TensorFlow/Keras, Matplotlib, Seaborn

## ⚙️ Methodology
### 1. Data Preprocessing
- **Outlier Treatment:** Handled using the whisker method.
- [cite_start]**Feature Engineering:** Dropped the `duration` column to prevent data leakage and ensure realistic model performance[cite: 28, 29].
- [cite_start]**Encoding:** Applied Label Encoding for binary features and One-Hot Encoding for categorical variables[cite: 37, 38].
- [cite_start]**Scaling:** Features were standardized using `StandardScaler` to ensure uniform influence[cite: 31, 35].
- [cite_start]**Data Splitting:** 80% Training and 20% Testing[cite: 39].

### 2. Model Training
Three classification models were trained and compared:
- [cite_start]**Logistic Regression:** Designed for binary classification and efficient with tabular data[cite: 43].
- [cite_start]**Decision Tree Classifier:** Captures non-linear relationships and provides high interpretability[cite: 46, 47].
- [cite_start]**Neural Network (MLP):** Capable of learning complex feature combinations and non-linear patterns[cite: 48, 49].

## 📈 Results and Comparison
[cite_start]All models achieved approximately 90% accuracy[cite: 52]. [cite_start]The **Decision Tree Classifier** emerged as the top performer for this specific task[cite: 53].

| Model | Accuracy | ROC-AUC |
|-------|----------|---------|
| **Decision Tree** | **89.98%** | **0.8002** |
| Logistic Regression | 89.79% | 0.7999 |
| Neural Network | 89.82% | 0.7724 |

[cite_start]*Note: Models still struggle with the minority class ('Yes') due to class imbalance (11.27% vs 88.73%)[cite: 25, 56].*

## 🚀 How to Run
1. Clone the repository: `git clone https://github.com/your-username/repository-name.git`
2. Install dependencies: `pip install -r requirements.txt`
3. Run the script: `python group_6_422project.py`

## 👥 Authors
- [cite_start]Ateaf Akram Chowdhury (ID: 23301335) [cite: 1]
- [cite_start]Kazi Rafid Nur Ferdous (ID: 23301305) [cite: 1]
