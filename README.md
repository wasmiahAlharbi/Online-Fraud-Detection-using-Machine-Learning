# 🕵️ Fraud Detection Machine Learning System

## 📖 Project Overview
This project builds a machine learning system to detect fraudulent online financial transactions using the IEEE-CIS Fraud Detection dataset.  
The dataset contains over 590,000 transactions with more than 400 features describing user behavior, devices, and transaction patterns.

The main challenges were:
- Severe class imbalance (fraud < 4%)
- High missing values
- High dimensionality

A complete ML pipeline was developed including data cleaning, preprocessing, feature encoding, SMOTE, PCA, and model training.

---

## 📊 Dataset

Source: IEEE-CIS Fraud Detection Dataset (Kaggle)

After merging:
- 590,540 records  
- 434 features  

Two tables:
- Transaction data  
- Identity data  

Merged using: TransactionID

---

##  Key Challenges
- Highly imbalanced classes  
- 50%–90% missing values in many features  
- Very large number of features  
- Noisy categorical data  

---

## 🛠 Preprocessing Steps

- Merging datasets  
- Dropping features with >90% missing values  
- Filling missing values:
  - Categorical → "unknown"
  - Numerical → -1  
- Encoding categorical features:
  - Ordinal Encoding  
  - Label Encoding  
  - Frequency Encoding  
- Feature scaling using StandardScaler  
- Handling imbalance using SMOTE  
- Dimensionality reduction using PCA (95% variance)

---

##  Dimensionality Reduction (PCA)

- Reduced features from 414 → ~78 components  
- Preserved 95% of data variance  
- Improved model performance and training speed  

---

##  Machine Learning Models

### Supervised Models:
- Random Forest  
- XGBoost  
- LightGBM (Best Overall)

### Unsupervised Model:
- Isolation Forest (Anomaly Detection)

---

##  Performance Summary

| Model | Precision (Fraud) | Recall (Fraud) | F1-score |
|------|------------------|---------------|---------|
| Random Forest | 0.18 | 0.71 | 0.29 |
| XGBoost (SMOTE) | 0.17 | 0.70 | 0.28 |
| XGBoost (Weighted) | 0.49 | 0.50 | 0.50 |
| LightGBM | 0.22 | 0.70 | 0.34 |
| Isolation Forest | 0.11 | 0.38 | 0.17 |

✅ Best balance achieved by optimized XGBoost and LightGBM.

---

##  Techniques Used

- Data Cleaning & Feature Engineering  
- SMOTE for class imbalance  
- PCA for dimensionality reduction  
- Tree-based models for high-dimensional data  
- Supervised & Unsupervised learning  

---

##  Tools & Technologies

- Python  
- Pandas, NumPy  
- Scikit-learn  
- XGBoost  
- LightGBM  
- Matplotlib & Seaborn  
- Jupyter Notebook  

---

##  Key Outcomes

- Successfully handled missing values and imbalance  
- Reduced dimensionality efficiently  
- Built high-performing fraud detection models  
- Demonstrated full ML pipeline from raw data to evaluation  

---

##  Future Improvements

- Deep Learning models  
- Real-time fraud detection system  
- Deployment as web application  
- Advanced feature selection
