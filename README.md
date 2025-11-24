# Regression_Boston-House-Price_KNR_DTR_SVR
Sure! Here’s a **well-structured README file** you can use for your housing price regression project:

---

# Housing Price Prediction Using Regression Models

## Project Overview

This project explores the use of three regression models—**KNN Regressor**, **Decision Tree Regressor**, and **SVM Regressor (SVR)**—to predict housing prices. The dataset contains features relevant to housing and the target variable is the median value of owner-occupied homes (in $1,000s). The goal is to compare model performance and recommend the best model for practical use by a housing agent.

## Models Used

1. **KNN Regressor**

   * Based on the nearest neighbors of a data point.
   * Sensitive to outliers and the choice of neighbors.

2. **Decision Tree Regressor**

   * Predicts using a tree structure that splits features.
   * Produces piecewise constant predictions.

3. **SVM Regressor (SVR)**

   * Uses support vectors to fit the data with a margin of tolerance.
   * Effective for capturing trends and handling outliers.

## Performance Metrics

| Model                   | R² (Test) | MAE (Test, $) | RMSE (Test, $) |
| ----------------------- | --------- | ------------- | -------------- |
| KNN Regressor           | 0.510     | 4,056         | 6,315          |
| Decision Tree Regressor | 0.615     | 3,222         | 5,597          |
| SVM Regressor (SVR)     | 0.759     | 2,629         | 4,429          |

* **R²**: Measures the proportion of variance in house prices explained by the model.
* **MAE**: Average error in prediction, in dollars.
* **RMSE**: Penalizes larger errors more heavily, giving insight into extreme deviations.

## Scatter Plot Observations

* **KNN Regressor**: Predictions are spread out; underpredicts high-priced houses and slightly overpredicts low-priced ones.
* **Decision Tree Regressor**: Shows horizontal bands due to piecewise constant predictions; accurate for mid-range prices but mispredicts extremes.
* **SVM Regressor (SVR)**: Points closely follow the diagonal line; accurately predicts both low- and high-priced houses with fewer extreme errors.

## Model Recommendation

Based on the performance metrics and scatter plot analysis, **SVM (SVR)** is recommended for predicting housing prices. It has the highest R² (0.759) and the lowest MAE ($2,629) and RMSE ($4,429), meaning predictions are both accurate on average and robust against extreme values—making it the most reliable choice for practical use by housing agents.

## How to Run

1. Install required libraries:

   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn
   ```
2. Load the dataset (`housing_data.csv`).
3. Train and evaluate the models using the provided script (`housing_regression.py`).
4. Visualize results with scatter plots (`scatter_plots.py`).

## Author

Nursyaza Nisa Binti Arfarizal

## License

This project is released under the MIT License.

