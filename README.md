# -Predicting-Home-Prices-in-Ames-Iowa
Machine learning regression project to predict residential home sale prices using historical housing data from Ames, Iowa


📌 Overview

This project applies linear and ridge regression models to predict housing prices based on property characteristics such as square footage, neighborhood, construction quality, and amenities.

A full preprocessing and modeling pipeline was implemented using Scikit-learn.

📂 Dataset

Source: Ames Housing Dataset

Location: Ames, Iowa

Samples: 2,564 homes

Target Variable: SalePrice

Each row represents one residential property sale.

🛠️ Tech Stack

Python

pandas

numpy

matplotlib

scikit-learn

category_encoders

🧪 Project Workflow

Data Wrangling and Cleaning

Feature Filtering

Time-Based Train/Validation Split

Baseline Modeling

Linear Regression Pipeline

Ridge Regression Pipeline

Model Evaluation

Test Set Prediction

🧩 Data Wrangling

Key preprocessing steps:

Parsed Yr_Sold as datetime index

Removed high-cardinality categorical features

Sorted data chronologically

Preserved temporal ordering to avoid leakage

📊 Exploratory Analysis

A scatter plot was created to visualize the relationship between:

Living Area (Gr_Liv_Area)

Sale Price (SalePrice)

This confirmed a strong positive correlation.

📐 Data Splitting Strategy

Time-based split:

Set	Period	Samples
Training	Before 2009	1,920
Validation	2009	644

This approach simulates real-world forecasting.

📈 Baseline

Baseline model predicts mean house price.

Baseline MAE: 58,503


All trained models significantly outperform this baseline.

🤖 Machine Learning Pipelines

Two regression pipelines were implemented.

Linear Regression Pipeline
OneHotEncoder
→ StandardScaler
→ LinearRegression

Ridge Regression Pipeline
OneHotEncoder
→ StandardScaler
→ Ridge(alpha=50)


Pipelines ensure consistent preprocessing.

🚀 Model Performance
Mean Absolute Error (MAE)
Model	Train MAE	Val MAE
Linear Regression	16,126	18,000
Ridge Regression	16,070	17,756
R² Score
Model	R² Score
Linear Regression	0.889
Ridge Regression	0.891

Ridge regression showed slightly better generalization.

🏆 Final Model

Ridge Regression was selected as the final model based on:

Lower validation MAE

Higher R² score

Better regularization

📤 Test Set Predictions

The final model generated predictions for 340 unseen homes.

Example output:

[216883.94, 104425.40, 161651.56, ...]


Test MAE met assignment requirements.

▶️ How to Run
Clone Repository
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name

Install Dependencies
pip install pandas numpy matplotlib scikit-learn category_encoders

Open Notebook
jupyter notebook


Run all cells in the main notebook.

⚠️ Limitations

No macroeconomic indicators

No renovation cost data

Linear model assumptions

Limited feature interactions

🌱 Future Improvements

Try ElasticNet regression

Add polynomial features

Feature selection methods

Gradient boosting models

Cross-validation tuning





👤 Author

Corey Williams BloomTech Data Science Program Sprint 1 - Regression

LinkedIn: www.linkedin.com/in/ corey-williams-alpha

GitHub: https://github.com/blackbox55

⭐ Why This Project Matters

This project demonstrates:

Regression modeling

Feature preprocessing

Time-series-aware validation

Pipeline design

Model comparison
