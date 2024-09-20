# F1-driver-position-prediction

This project predicts the finishing position of an F1 driver in a race based on historical race and driver data. It includes various features such as driver status, race name, circuit name, and driver performance metrics.

**Table of Contents:**
Overview
Dataset
Project Structure
Features and Model
Getting Started
Requirements
Installation
Usage
Model Performance


**Overview**
This project aims to predict the position of an F1 driver in a race by applying machine learning algorithms such as Gradient Boosting, Random Forest, and Decision Tree regressors. The predictions are based on a variety of features like the race name, driver name, circuit, and more. The project utilizes both numerical and categorical feature engineering techniques such as frequency encoding and target encoding.


**Dataset**
The dataset is scraped from the Ergast API. We have included the data since 2015. The dataset includes the following key features:
Race name, circuit name,Driver name, driver status, Number of laps, grid position, points, Fastest lap information, race year, Status categories (e.g., Finished, Retired, Disqualified)


**Data Preprocessing**
Missing values were handled using appropriate imputation techniques.
Various encodings were applied to categorical features, including frequency encoding and target encoding.


**Project Structure**

├── Data Scraped
├── Downloaded CSV File
├── Understand the Data
├── Preprocessing:
│   ├── Dropping columns
│   ├── Combining columns
│   ├── Filling null values using grouped mean/median and -1 for missing historical data
├── Checking Covariance
├── Performing EDA
├── Pipeline Creation:
│   ├── Decision Tree
│   ├── Gradient Boost
│   ├── Random Forest
├── Hyperparameter Tuning by Grid Search
├── Best Model Selection
├── Prediction
├── Evaluation
└── User Interaction


**Model**

Machine Learning Models
The following models were implemented using scikit-learn:
Gradient Boosting Regressor: The best-performing model, achieving high R² scores.
Random Forest Regressor
Decision Tree Regressor
Model performance was evaluated using various metrics such as R², Mean Absolute Error (MAE), and Mean Squared Error (MSE).


**Getting Started**
Requirements
Ensure you have the following Python packages installed:
requests
pandas
numpy
seaborn
matplotlib
google.colab
io
sklearn
category_encoders
joblib


**Model Performance**
The best model, Gradient Boosting Regressor, achieved the following results:
Mean Squared Error: 1.536040105107755
Mean Absolute Error: 0.7145893601071235
R^2 Score: 0.9540938651985433
Explained Variance Score: 0.9542705960318426
Median Absolute Error: 0.19433114501832005
Other models (Random Forest and Decision Tree) were also tested, but Gradient Boosting produced the most consistent results.
