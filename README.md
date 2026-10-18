# Telco Churn Prediction

An end-to-end machine learning project for predicting customer churn in a telecommunications company. The project is currently in the exploratory data analysis stage.

## Project Goal

Analyze customer characteristics, investigate patterns associated with churn, and eventually build and deploy a machine learning model to predict customer churn.

## Dataset

This project uses the Telco Customer Churn dataset, containing 7,043 customer records and 21 columns. The target variable is `Churn`(Yes or No).

The raw CSV is not tracked in Git. To reproduce the analysis, place the dataset at:

`data/telco_customer_churn.csv`

## Initial Findings

* **Churn:** 1,869 customers (26.54%) churned; 5,174 (73.46%) did not. The target is imbalanced, so accuracy alone will not be sufficient to evaluate a future model.

* **Duplicates:** No fully duplicated rows were detected.

* **Data quality:** `TotalCharges` was initially stored as text. Eleven blank values were found, all belonging to customers with `tenure = 0`.

* **Cleaning decision:** `TotalCharges` was converted to a numeric type. Those eleven missing values were replaced with 0.0, based on the assumption that customers with zero tenure have not accumluated charges. No row were removed.

These are preliminary observations, not model results.


## Project Roadmap

### Exploratory Data Analysis
- [x] Dataset overview
- [x] Data quality assessment
- [x] Data cleaning
- [x] Target variable analysis
- [ ] Numerical feature analysis
- [ ] Categorical feature analysis
- [ ] Feature relationships with churn
- [ ] Key findings and EDA summary

### Machine Learning & Deployment
- [ ] Feature engineering and preprocessing pipeline
- [ ] Model training
- [ ] Model evaluation
- [ ] API development with FastAPI
- [ ] Dockerization
- [ ] Deployment


## Tech Stack

- Python
- Pandas
- Numpy
- Matplotlib
- Scikit-learn
- FastAPI
- Docker

## Project Structure

* `notebooks/01_eda.ipynb` exploratory data analysis and initial cleaning
* `data/README.md` dataset placement instructions
* `requirements.txt` Python dependencies
* `.gitignore` files excluded from version control

## Current Status

**In Progress:** Exploratory Data Analysis. Initial dataset exploration, data quality checks, cleaning, and target distribution analysis have been completed. Numerical and categorical feature analysis is next.