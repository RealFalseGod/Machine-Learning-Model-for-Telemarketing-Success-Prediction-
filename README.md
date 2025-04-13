# Predicting Success of Bank Telemarketing Campaigns

This project involves building a machine learning pipeline to predict the success of telemarketing campaigns conducted by a bank. The dataset is sourced from a Kaggle competition and includes customer demographics, previous campaign information, and economic indicators.

## 📁 Dataset

The dataset contains two files:
- `train.csv`: Used for training the model. Contains the target variable.
- `test.csv`: Used for testing/prediction. Does not contain the target variable.

## 🧠 Objective

To classify whether a client will subscribe to a term deposit based on campaign-related and customer-related features.

## 🔍 Exploratory Data Analysis (EDA)

- Analyzed categorical variables (`job`, `marital`, `education`, etc.) using countplots.
- Analyzed numerical features (`age`, `balance`, etc.) using histograms and correlation heatmaps.
- Identified null values mainly in `contact` and `poutcome`.
- Observed class imbalance in the `target` variable.

## 🧹 Preprocessing

- Dropped `contact`, `poutcome`, and `last contact date` due to high missing values or irrelevance.
- Used `ColumnTransformer` and `Pipeline` for:
  - One-hot encoding of categorical features.
  - Scaling numerical features.
  - SimpleImputer for missing value handling.
- Noted a missing feature in the preprocessing pipeline as part of Version 1.

## 🧪 Models Used

### 1. Dummy Classifier
- Baseline model to register a benchmark score.
  
### 2. Random Forest Classifier
- Performed well initially.
- Hyperparameter tuning with `RandomizedSearchCV` improved the performance.
- Achieved a score of **0.70210**.

### 3. Logistic Regression
- Basic implementation without tuning.
- Lower performance than Random Forest.
- Score: **0.56798**.


## ✅ Conclusion

- Random Forest performed the best among the tried models.
- Preprocessing pipeline can be improved by ensuring all necessary columns are included.
- Dataset is imbalanced; class balancing or weighted models can improve results further.

## 🔧 To Do

- Improve feature engineering.
- Address class imbalance.
- Try advanced models like XGBoost or LightGBM.
- Explore time-series patterns if relevant.

---

Made with 💻 by Bhagwansingh chavan


