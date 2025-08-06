# 💼 ML-Tax-Incentive-Approval-Model

A PySpark-based machine learning pipeline to predict tax credit approval eligibility under the New Market Tax Credit (NMTC) program. Built using public finance data and designed for FinTech analyst portfolios.

## 🚀 Overview

This project simulates a FinTech decision system that classifies whether a record should receive NMTC benefits. It uses logistic regression in PySpark's MLlib and outputs model predictions for further analysis.

## 📁 Project Structure

- `data/NM_Taxcred.csv` — input dataset  
- `predictions/tax_credit_predictions.csv` — model output  
- `notebooks/tax_credit_classifier.ipynb` — Jupyter notebook  
- `README.md` — project summary  
- `requirements.txt` — required libraries

## 🔧 Technologies Used

- PySpark
- Spark MLlib
- Pandas
- Jupyter Notebook

## 🧠 ML Pipeline

1. Load and clean data
2. Label encode “New Market Tax Credit” (Yes/No → 1/0)
3. Assemble features with VectorAssembler
4. Train logistic regression classifier
5. Evaluate using AUC
6. Export predictions to CSV

## 📊 Sample Output

| OBJECTID | label | prediction | probability         |
|----------|-------|------------|---------------------|
| 1001     | 1     | 1.0        | [0.03, 0.97]        |
| 1043     | 0     | 0.0        | [0.89, 0.11]        |




## ⚙️ How to Run This Project

1. **Clone the repository:**
```bash
git clone https://github.com/Chandraishaan80/ML-Tax-Incentive-Approval-Model.git
cd ML-Tax-Incentive-Approval-Model

--Install the required dependencies:
pip install -r requirements.txt
--Launch Jupyter Notebook
jupyter notebook

--Open the notebook
Navigate to notebooks/tax_credit_classifier.ipynb

--Run all cells step-by-step:

Initialize Spark
Load and clean the dataset
Encode the target column (New Market Tax Credit)
Assemble features
Train logistic regression model
Evaluate with AUC
Export predictions
--Output Location:
CSV file with predictions is saved to:
predictions/tax_credit_predictions.csv

