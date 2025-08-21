# 🚀 Fraud Detection in Financial Transactions

> End-to-end machine learning project to detect fraudulent transactions, handle class imbalance, and derive business insights.
> You can download the dataset from https://drive.usercontent.google.com/download?id=1VNpyNkGxHdskfdTNRSjjyNa5qC9u0JyV&export=download&authuser=0

## 📌 Overview
This repository contains a production-style workflow for **fraud detection** on a large-scale transactions dataset (~**6.3M+ rows**).  
It covers **data cleaning, EDA, feature engineering, class imbalance handling (SMOTE), model training (Logistic Regression, Random Forest, XGBoost)**, and **business recommendations** backed by model interpretability.

## 🎯 Objectives
- Clean and validate raw data (missing values, outliers, multicollinearity).
- Perform **EDA** to understand fraud patterns by amount, time (`step`), and transaction `type`.
- Engineer domain features (e.g., **balanceDiffOrig**, **balanceDiffDest**) and encode categorical variables.
- Address severe **class imbalance** with **SMOTE**.
- Train & compare models (**LogReg**, **RandomForest**, **XGBoost**) with appropriate metrics.
- Communicate **key drivers of fraud** and **prevention strategies** for stakeholders.

## 🛠️ Tech Stack
- **Language:** Python  
- **Core:** Pandas, NumPy  
- **ML:** scikit-learn, XGBoost, imbalanced-learn (SMOTE)  
- **Viz:** Matplotlib, Seaborn  
- **Environment:** Jupyter Notebook

## 📂 Repository Structure
fraud-detection/
│── notebook/
│ └── Fraud_Detection_Assignment.ipynb
│── requirements.txt
│── README.md
│── .gitignore

bash
Copy
Edit

## ⚙️ Setup & Usage
1. **Clone the repo**
   ```bash
   git clone https://github.com/<your-username>/fraud-detection-ml.git
   cd fraud-detection-ml
Create & activate a virtual environment (recommended)

bash
Copy
Edit
python -m venv .venv
# Windows
.venv\Scripts\activate
# macOS/Linux
source .venv/bin/activate
Install dependencies

bash
Copy
Edit
pip install -r requirements.txt
Add dataset

Place the CSV in data/ (or update the notebook path accordingly).

Large files should not be committed—keep them local or link to their source in data/README.md.

Run the notebook

bash
Copy
Edit
jupyter notebook
Open notebook/Fraud_Detection_Assignment_Updated.ipynb and execute cells sequentially.

🧪 Methodology (What’s Inside the Notebook)
Data Cleaning: nulls, outliers (IQR/Z-score), multicollinearity (correlation/VIF).

EDA: class imbalance, distribution plots, correlation heatmap, type-wise fraud.

Feature Engineering: one-hot encode type, create balanceDiffOrig & balanceDiffDest.

Imbalance Handling: SMOTE on the training set.

Models: Logistic Regression (baseline), Random Forest, XGBoost.

Evaluation: Precision, Recall, F1-score, ROC-AUC, Confusion Matrix, ROC/PR curves.

Interpretability: Feature importance charts; translate signals into business language.

Recommendations: real-time anomaly detection, MFA for high-value transactions, risk-based limits.

📊 Results 
Model	Precision	Recall	F1-Score	ROC-AUC
Logistic Regression				
Random Forest				
XGBoost				

Tip: For imbalanced problems, emphasize Recall / PR-AUC alongside ROC-AUC.

🖼️ Key Visualizations
Fraud vs Non-Fraud distribution

Transaction type distribution

Correlation heatmap

Feature importance (tree-based models)

ROC / Precision-Recall curves

📚 Dataset
Columns include: step, type, amount, nameOrig, oldbalanceOrg, newbalanceOrig, nameDest, oldbalanceDest, newbalanceDest, isFraud (target), isFlaggedFraud.

✅ Best Practices Followed
Reproducible environment via requirements.txt

Clear separation of analysis (EDA) and modeling

Business-oriented insights with measurable evaluation criteria

🤝 Contributing
Issues and PRs are welcome. For major changes, please open an issue first to discuss what you’d like to change.
