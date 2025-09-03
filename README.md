# Germany-Housing-Price-Prediction
## Introduction
This project aims to build a **predictive model for rental prices (price_per_sqm)** in Germany using housing data.  

**Objectives:**
- Explore and preprocess the dataset (EDA, missing value handling, encoding, scaling).
- Build regression models (Linear Regression, Ridge Regression).
- Evaluate model performance and select the best approach.

---

## Dataset
The dataset contains different types of features:

- **Boolean variables (True/False):**  
  `['hasKitchen', 'garden', 'lift', 'cellar', 'newlyConst', 'balcony']`

- **Categorical variables:**  
  `['state', 'typeOfFlat', 'heatingType', 'condition']`

- **Continuous variables:**  
  `['noRooms', 'floor', 'yearConstructed']`

- **Target variable:**  
  `price_per_sqm` (rental price per square meter).

---

## Methodology
1. **Data Preprocessing**
   - Handle missing values.
   - Encode categorical variables using One-Hot Encoding.
   - Keep Boolean variables as binary (0/1).
   - Standardize continuous variables using StandardScaler.

2. **Modeling**
   - Use **Linear Regression** as a baseline.
   - Apply **Ridge Regression** to handle potential overfitting.
   - Leverage `Pipeline` + `GridSearchCV` to optimize hyperparameters (`alpha`).

3. **Evaluation**
   - Use **Cross-Validation R²** for model selection.
   - Measure performance on test data using **Mean Squared Error (MSE)**.

---

## 🧮 Results
- **Best alpha:** `1`  
- **Best R² (CV):** `0.573`  
- **Test MSE:** `4.82`  

👉 Ridge Regression with `alpha=1` showed stable and balanced performance between training and testing.

---

## Future Work
- Experiment with alternative models (Lasso, ElasticNet, RandomForest, XGBoost).
- Feature engineering (interaction terms, log transformations).
- Evaluate models with additional metrics (MAE, RMSE, R²).
- Improve handling of missing values and rare categories.

---
