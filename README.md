🌐 **Language:** English | [Español](README_ES.md)

# Customer Churn Prediction

Machine Learning project focused on predicting customer churn and identifying customer segments with higher churn risk.

This project was developed as part of the **Data Science program at Henry** and combines exploratory data analysis, supervised learning, model optimization, unsupervised learning, and feature engineering to address a customer retention business problem.

## Business Problem

The project is based on a fictional digital banking scenario with **10,000 active customers** and an annual customer churn rate of approximately **20%**.

The objective is to develop a predictive approach capable of identifying customers with a higher probability of leaving the bank, providing useful information to support customer retention strategies.

## Project Workflow

The project was developed through three main stages:

### 1. Exploratory Data Analysis & Logistic Regression

- Exploratory Data Analysis (EDA)
- Data quality analysis
- Analysis of class imbalance
- Categorical variable encoding
- Train/test split
- Feature scaling
- Logistic Regression as a baseline model
- Evaluation using classification metrics

### 2. Machine Learning Models & Optimization

Several classification algorithms were trained and compared:

- Logistic Regression
- Random Forest
- XGBoost
- LightGBM
- CatBoost

Model performance was evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC
- Confusion Matrix

Hyperparameter optimization was also performed using **Optuna**.

### 3. Unsupervised Learning & Feature Engineering

Customer segmentation techniques were explored using:

- K-Means
- DBSCAN
- PCA
- t-SNE

The clustering analysis was used to identify customer groups with different churn behavior.

A new feature, `cluster_risk_priority`, was created to incorporate information from customer segmentation into the analysis.

## Key Results

The Logistic Regression baseline achieved:

- **Accuracy:** 80.80%
- **ROC-AUC:** 77.48%
- **Recall:** 18.67%

After comparing and optimizing more advanced models:

- **XGBoost achieved a ROC-AUC of 86.79%**
- **LightGBM achieved the highest Recall at 49.63%**

The XGBoost feature importance analysis identified the following variables among the most relevant predictors:

- `IsActiveMember`: 27.39%
- `NumOfProducts`: 26.75%
- `Age`: 22.54%

Customer segmentation also identified a higher-risk group associated with customers from Germany, with a churn rate of **32.44%**.

These results show how supervised and unsupervised Machine Learning techniques can complement each other when analyzing customer churn and supporting retention strategies.

## Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Statsmodels
- XGBoost
- LightGBM
- CatBoost
- Optuna
- Jupyter Notebook

## Project Structure

```text
customer-churn-prediction/
│
├── data/
│   ├── Churn_Modelling.csv
│   └── processed datasets
│
├── notebooks/
│   ├── 1_EDA_RegresionLogistica.ipynb
│   ├── 2_GradientBoosting_Optimizacion.ipynb
│   └── 3_AprendizajeNoSupervisado.ipynb
│
├── reports/
│   ├── Reporte_Modelos.pdf
│   └── Recomendaciones_Reporte_Modelos.pdf
│
├── .gitignore
├── requirements.txt
└── README.md
```

## Installation

Clone the repository:

```bash
git clone https://github.com/Deiberlyn/customer-churn-prediction.git
```

Create and activate a virtual environment, then install the required dependencies:

```bash
pip install -r requirements.txt
```

The notebooks can then be executed in order from the `notebooks/` directory.

## Author

**Deiberlyn Nin**

Data Science Junior  
Python | SQL | Machine Learning

- GitHub: https://github.com/Deiberlyn
- LinkedIn: https://www.linkedin.com/in/deiberlyn-nin-b893b1432/