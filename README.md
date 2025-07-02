# Predictive-Modeling-Gems-Price-Holiday-Package-Purchase
Predicted gem prices using multivariate regression and customer likelihood of holiday package purchase using logistic regression and LDA. Informed marketing and pricing strategies.
# 🔍 Predictive Modelling: System Performance & Contraceptive Method Use

---

## 🚀 Project Overview
📈 **Repo:** `Predictive-Modelling-Linear-Logistic-LDA-CART`

This project includes:

1. **Predicting System Performance:**  
   Built a linear regression model to predict CPU user mode usage (`usr`) on a Sun workstation using system metrics.

2. **Predicting Contraceptive Method Use:**  
   Used Logistic Regression, LDA, and CART to predict contraceptive method usage among Indonesian married women.

---

## 🖥️ Part 1: Predicting CPU Usage with Linear Regression

### 🏢 Business Problem
For a multi-user university department using Sun Sparcstation, predicted the percentage of CPU time in user mode (`usr`) based on system activity metrics.

### 🔍 Dataset
- 23 features: system calls, memory reads/writes, page faults, queue size, etc.
- 8192 records.

### 📝 Workflow & Highlights
- **Data Cleaning:**  
  - Handled missing values in `rchar` & `wchar` by imputing means.
  - Verified no duplicate rows.
- **EDA:**  
  - Correlation matrix revealed strong ties among `lread`, `lwrite`, `scall`.
  - Boxplots & pairplots helped identify outliers and relationships.
- **Feature Engineering:**  
  - Converted `runqsz` into dummy variables indicating CPU-bound processes.

### 🔥 Modelling & Results
| Model     | R² | Adj R² | RMSE |
|-----------|----|--------|------|
| Model 1 (all vars) | 0.794 | 0.793 | ~4.45 |
| Model 2 (removed low-impact vars) | 0.793 | 0.792 | ~4.45 |
| Model 3 (removed high VIF vars)   | 0.720 | 0.719 | ~5.18 |

✅ **Insights:**
- Removing high-VIF variables reduced performance, suggesting they were crucial despite multicollinearity.
- About **79% of the variance** in `usr` was explained by system metrics.

💡 **Business Impact:**  
- Understanding key drivers like `lread`, `lwrite`, `scall` helps optimize system resource allocation, improve performance, and cut costs.

---

## 🚼 Part 2: Predicting Contraceptive Method Usage

### 🏢 Business Problem
For the Ministry of Health of Indonesia, predicted whether married women use contraceptive methods based on demographics & socio-economic factors.

### 🔍 Dataset
- 1,393 records after removing duplicates.
- Features: wife & husband education, number of children, religion, working status, standard of living, media exposure.

### 📝 Workflow & Highlights
- Imputed missing values with medians for `wife_age` & `no_of_children`.
- Used LabelEncoder to convert categorical vars.
- Train-test split (70:30).
- Explored with boxplots & pairplots.

### 🚀 Models & Results
| Model               | Train Accuracy | Test Accuracy | Recall |
|----------------------|----------------|---------------|--------|
| Logistic Regression   | ~65%           | ~67%          | ~86%   |
| LDA                   | ~65%           | ~67%          | ~87%   |
| CART                  | ~98% (overfit) | ~66%          | ~65%   |

✅ **Insights:**
- Logistic & LDA models offered stable, balanced performance across metrics.
- CART overfitted on training but dropped on unseen data.

💡 **Business Impact:**  
- Helps family planning agencies identify segments likely to adopt contraception, allowing targeted outreach and resource allocation.

---

## 📈 Key Visualizations
- 📊 Correlation heatmaps & boxplots (system metrics & contraceptive data)
- 🧩 Pairplots to uncover relationships
- 📉 ROC curves comparing Logistic, LDA & CART
- Please check the PRoject report attached with this repository for complete visualisation

---

## 🛠️ Tools & Skills Covered
- 🐍 Python: pandas, numpy, seaborn, matplotlib, scikit-learn
- 📈 Regression & Classification: OLS, Logistic Regression, LDA, CART
- 🔍 Model assessment via R², RMSE, accuracy, recall, ROC-AUC
- 📝 Business storytelling & actionable recommendations

---

## ⚙️ How to Run
- Open `Predictive Modelling(Linear Regression)_Issac Abraham.ipynb` for system performance regression.
- Open `Predictivemodelling_Logistic regression_LDA_CARTIssac Abraham.ipynb` for contraceptive prediction models.

---

## 🤝 About Me
I completed this project independently, showcasing strong skills in data cleaning, exploratory analysis, machine learning, and business-oriented insights.

🔗 [LinkedIn](https://linkedin.com/in/yourprofile)

---

✅ **Thanks for exploring my predictive modelling work!**
