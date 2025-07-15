DEFAULT OF CREDIT CARD CLIENTS

Project Description
Overview
This project aims to develop and evaluate predictive models for assessing the likelihood that a credit card client will default on their next payment. Leveraging the “Default of Credit Card Clients” dataset from the UCI Machine Learning Repository, we walk through the full data science pipeline—from raw data ingestion through cleaning, exploratory analysis, model training, and interpretation—culminating in actionable insights for risk management.
________________________________________
Data Preparation
1.	Loading & Inspection
o	Imported the Excel file, skipping an initial title row to correctly capture column names.
2.	Cleaning
o	Removed an irrelevant ID column.
o	Dropped duplicate records to prevent bias.
o	Re coded invalid categories in EDUCATION and MARRIAGE into an “Others” group.
o	Verified there were no missing values.
3.	Export
o	Saved the cleaned dataset as cleaned_credit_card_data.csv for reproducibility.
________________________________________
Exploratory Data Analysis (EDA)
•	Descriptive Statistics: Summary metrics (mean, standard deviation, quartiles) for all numeric features.
•	Class Balance: Visualized default vs. non-default counts to assess imbalance.
•	Feature Relationships:
o	Correlation heatmap to identify multicollinearity.
o	Histograms and boxplots for credit limits, stratified by default status.
o	Categorical breakdowns (gender, education level, marital status) against default rates.
•	Group Comparisons: Averaged features by default status to highlight key differences.
________________________________________
Modeling & Evaluation
1.	Data Split & Scaling
o	80/20 train-test split, stratified by the default rate.
o	Standardized numeric features for algorithms sensitive to scale.
2.	Algorithms
o	Logistic Regression: Interpretable baseline with coefficient analysis.
o	XGBoost: High-performance gradient boosted trees.
o	Support Vector Machine (SVM): Margin based classification after scaling.
3.	Metrics & Visuals
o	Accuracy, precision, recall, and F1 score on the test set.
o	ROC and Precision–Recall curves (with AUC) to compare discrimination ability.
o	Confusion matrices for raw performance counts.
4.	Interpretability
o	Bar charts of feature importances (XGBoost) and coefficient magnitudes (Logistic Regression) to explain model decisions.
________________________________________
Key Findings & Impact
•	Performance: All three models achieved ~81% accuracy, with trade offs between catching defaulters (recall) vs. avoiding false alarms (precision).
•	Drivers of Default: Features such as credit limit, past payment history, and bill amount emerged as the strongest predictors.
•	Business Value: The models and interpretability analyses provide a transparent, data driven tool for credit risk assessment, enabling banks to flag high risk clients before issuing credit.
This end to end project demonstrates a robust approach to credit risk modeling, blending best practices in data cleaning, visualization, algorithm selection, and explainability to deliver trustworthy, actionable insights.


