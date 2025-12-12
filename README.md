Telecom Customer Churn Prediction
End-to-End ML Pipeline (Notebook + Python Script Workflow)
Model Used: Random Forest
Final ROC AUC: 0.82


📌 Overview
This project predicts customer churn for a telecom company using machine learning.
It includes a complete production-grade pipeline, covering:
•	Data cleaning & preprocessing
•	Feature engineering
•	Handling imbalanced data using SMOTE
•	Stratified K-Fold Cross Validation (K=5)
•	Hyperparameter tuning using RandomizedSearchCV
•	Model training (Random Forest)
•	Model evaluation (Classification Report, Confusion Matrix, ROC Curve)
•	Saving and loading the final model
•	Both notebook-based exploration and a python script-based workflow

🎯 Goal
Predict whether a customer will churn (1) or not churn (0), enabling telecom companies to:
•	Reduce customer churn
•	Improve customer retention strategies
•	Identify at-risk customers proactively

Dataset Description
Common columns in telecom churn datasets:
•	Demographic: gender, SeniorCitizen, Partner, Dependents
•	Services: InternetService, OnlineSecurity, OnlineBackup, TechSupport, PhoneService
•	Account: Contract, PaymentMethod, tenure
•	Billing: MonthlyCharges, TotalCharges
•	Target: Churn → 1 (Yes), 0 (No)
⚙️ Data Preprocessing
Preprocessing included:
•	Converting categorical columns using OneHotEncoding
•	Scaling numeric features using StandardScaler
•	Dropping irrelevant columns (e.g., customerID)
•	Fixing improper numeric values (e.g., " " in TotalCharges)
•	Creating new meaningful features (optional)


🧮 Imbalance Handling – SMOTE
Churn datasets are typically imbalanced (~25–30% churn).
To fix this, SMOTE was applied only to the training data:


🔁 Cross-Validation – Stratified K-Fold
Used to ensure both classes are represented equally in each fold:


🔧 Hyperparameter Tuning
RandomizedSearchCV was used to find the best Random Forest settings:


🤖 Final Model: Random Forest
•	The model correctly distinguishes churn vs non-churn 82% of the time.
•	Performance for churn class is typical and can be further improved using threshold tuning, class weights, and XGBoost.

