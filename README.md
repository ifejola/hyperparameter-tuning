# Hyperparameter Tuning Using GridSearchCV

## Project Overview

This project explores hyperparameter tuning to improve the predictive performance of a Decision Tree Regression model.

Using housing data, I implemented GridSearchCV to evaluate different combinations of model settings and identify parameters that support better generalization.

## Dataset

**housing.csv**

The dataset contains housing information, including:

- Geographic location
- Housing median age
- Total rooms and bedrooms
- Population and households
- Median income
- Median house value (target variable)

## Tools & Libraries

Python | Pandas | Matplotlib | Scikit-learn

## Methodology

### 1. Data Preparation

- Loaded and explored the housing dataset.
- Removed rows containing missing values.
- Selected eight numerical features.
- Split the data into 80% training and 20% testing.

### 2. Initial Decision Tree Model

Trained a Decision Tree Regressor with the following parameters:

- max_depth = 10
- min_samples_split = 20
- min_samples_leaf = 10

### 3. Hyperparameter Tuning

Used GridSearchCV with 5-fold cross-validation to evaluate combinations of:

| Hyperparameter | Values Tested |
|---|---|
| max_depth | 5, 10, 15, 20 |
| min_samples_split | 5, 10, 20, 30 |
| min_samples_leaf | 5, 10, 20, 25 |

Used R² as the scoring metric.

### 4. Final Model

Trained a final Decision Tree Regressor using:

- max_depth = 15
- min_samples_split = 20
- min_samples_leaf = 5

### 5. Model Evaluation

Evaluated the model using R² and Mean Absolute Error (MAE).

## Results

| Metric | Result |
|---|---:|
| Training R² | 0.8054 |
| Test R² | 0.7312 |
| Training MAE | $34,361.28 |
| Test MAE | $40,685.62 |

The final model achieved a test R² of approximately 0.73, explaining about 73% of the variation in house values in the test dataset.

The test MAE indicates an average absolute prediction error of approximately $40,686.

## Learning Outcomes

- Understanding model parameters versus hyperparameters
- Applying GridSearchCV
- Using cross-validation
- Evaluating overfitting and underfitting
- Comparing training and testing performance

## Future Improvements

- Compare initial and tuned model performance.
- Use the best parameters returned directly by GridSearchCV.
- Explore RandomizedSearchCV.
- Evaluate additional regression models.
