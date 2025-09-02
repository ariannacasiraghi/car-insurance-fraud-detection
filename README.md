# Car Insurance Fraud Detection

## Project Overview
This project was completed as part of the <u>**Data Science module in the MSc in AI program at the University of Leeds**</u>. The task was to build two models for a car insurance company aimed to predict fraudulent claims using historical data, compare them, and evaluate the financial implications of deploying the best model.

## Objectives
- <u>**Analyse a historic dataset**</u> containing customer and claim information.
- <u>**Develop and compare two predictive models**</u> (I selected Random Forest & Multilayer Perceptron).
- <u>**Evaluate the models**</u> using adequate performance metrics and select the best model.
- <u>**Recommend a pricing model**</u> that, based on the company’s business requirements,  balances fraud detection accuracy with customer retention and profitability.

## Datasets
- The dataset was provided by the University of Leeds for academic purposes.
- It contained customer demographics, policy details, vehicle information, and claims data, with labels indicating whether a claim was fraudulent.
- Due to licensing restrictions, <u>**the dataset cannot be shared publicly**</u>.

## Methods
- <u>**Preprocessing**</u>: merging data sources, feature selection, encoding (one-hot and ordinal), scaling, imputation. Most preprocessing steps were applied using pipelines after train/test split to prevent data leakage.
- <u>**Models**</u>: Random Forest (best), Multilayer Perceptron. Both models tuned using grid search and cross validation.
- <u>**Metrics**</u>: balanced accuracy, recall, F1, confusion matrix, precision–recall curves.
- <u>**Pricing model**</u>: built based on the following considerations. (i) false positives = genuine claims flagged as fraud result in lost customers; (ii) false negatives = fraudulent claims missed result in financial loss; (iii) Company requirement: “gross profit must be double the claims paid”.

## Results
- <u>**Best model**</u>: Random Forest (balanced accuracy: 89%, balanced error rate: 11%); small overfitting (<5% difference between train, test, and CV).
- <u>**Impact**</u>: Model saves ~42% compared with paying all claims.
- <u>**Business insight**</u>: Lowering the decision threshold for the Random Forest model (precision–recall curve) increases financial savings despite decreased customer retention.


## How to Run
- git clone [car-insurance-fraud-detection](https://github.com/ariannacasiraghi/car-insurance-fraud-detection.git)
- `pip install -r requirements.txt`
- `jupyter notebook car-insurance-fraud-detection.ipynb`
