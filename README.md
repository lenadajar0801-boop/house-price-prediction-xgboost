# House Price Prediction using XGBoost Regression

## Project Overview

This project focuses on predicting house prices using machine learning techniques, with a strong emphasis on improving performance through advanced models.

Building on baseline models such as Linear Regression, Random Forest, and Gradient Boosting, this project introduces XGBoost as the final model to achieve higher predictive accuracy.

The dataset is sourced from Kaggle’s House Prices competition and includes a mix of numerical and categorical features describing residential homes.

---

## Objective

To build an accurate house price prediction model by comparing baseline models and improving performance using XGBoost.

---

## Dataset

Source: https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques

Dataset Used:

* train.csv

Dataset characteristics:

* Contains 1460 records
* Total columns: 81 (before preprocessing)
* Includes numerical and categorical variables
* Target variable: SalePrice

---

## Tools & Technologies

* Python
* Pandas, NumPy
* Scikit-learn
* XGBoost
* Matplotlib, Seaborn
* Jupyter Notebook

---

## Data Preprocessing

### Steps Performed

* Explored dataset using `shape`, `info()`, and `describe()`
* Identified missing values
* Dropped columns with excessive missing data:

  * PoolQC
  * MiscFeature
  * Alley
  * Fence
* Filled missing values:

  * Numerical → median
  * Categorical → mode
* Converted categorical variables using one-hot encoding
* Reduced multicollinearity using `drop_first=True`
* Defined features (X) and target (y)

### Explanation

Data preprocessing ensures the dataset is clean and suitable for machine learning. Proper handling of missing values and categorical variables improves model performance and stability.

---

## Model

### Models Used

* Linear Regression (Baseline)
* Random Forest Regressor
* Gradient Boosting Regressor
* XGBoost Regressor (Final Model)

### Steps Performed

* Split dataset into training (80%) and testing (20%)
* Trained baseline models
* Evaluated baseline models using R² score
* Trained XGBoost model
* Generated predictions
* Evaluated XGBoost using MAE and R²

---

## Results

| Model             | R² Score   |
| ----------------- | ---------- |
| Linear Regression | ~0.64      |
| Random Forest     | ~0.89      |
| Gradient Boosting | ~0.897     |
| XGBoost           | **~0.907** |

---

## Visualization

### Actual vs Predicted (XGBoost)

* Scatter plot comparing actual vs predicted house prices
* A diagonal line represents perfect prediction
* Most points align closely with the diagonal line

### Interpretation of Visualization

* Strong alignment indicates high model accuracy
* Small deviations show prediction error
* Few outliers remain but are minimized

---

## Interpretation

XGBoost achieved the best performance with an R² score of approximately 0.907, explaining over 90% of the variance in house prices.

The model significantly improved accuracy compared to baseline models, demonstrating the effectiveness of advanced boosting techniques.

---

## Insights

* Ensemble methods outperform simple linear models
* Gradient Boosting performs slightly better than Random Forest
* XGBoost provides the highest accuracy
* Proper preprocessing greatly impacts model performance
* Non-linear relationships are important in house price prediction

---

## Limitations

* Dataset does not include all real-world factors
* Some missing values may still affect predictions
* No hyperparameter tuning was applied
* Outliers still exist

---

## Future Improvements

* Apply hyperparameter tuning (GridSearchCV)
* Perform feature engineering
* Use cross-validation
* Handle outliers more effectively
* Try stacking or blending models

---

## Conclusion

This project demonstrates how advanced machine learning models significantly improve house price prediction accuracy.

XGBoost achieved the best performance, making it the most effective model for this dataset.

The project highlights the importance of model selection and preprocessing in regression problems.

---

## Author

Allen Adajar
Cost Accountant | Data Analyst | Aspiring Data Scientist

GitHub: https://github.com/lenadajar0801-boop
