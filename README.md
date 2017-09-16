# Weekly Retail Gas Price Prediction

Predictive model for weekly retail gas prices in different states and cities.

Predictors: crude oil and gasoline spot prices, stocks, and supplies.

Data source: [U.S. Energy Information Administration](https://www.eia.gov)

## Table of Contents
### 1. Multivariate Rolling Regression Model for National Retail Gas Price

* Set-up
* Differentiation
* Predictors
    * Correlation with Predictors
    * Select Predictors by LARS Path
    * Correlation betweeen Predictors
    * Selected Predictors
* Rolling Regression
    * Change of Regression Coefficients over time
* Test in Training Period
  + Metric 1: Correlation of Predicted and Actual Log Return
  + Outlier: Hurrican Katrina
  + Metric 2: Precision, Recall, and Accuracy of Predicting Price Move Directions
* Test in Cross-Validation Period
  + Metric 1: Correlation of Predicted and Actual Log Return
  + Metric 2: Precision, Recall, and Accuracy of Predicting Price Move Directions

### 2. ARIMA Model for National Retail Gas Price

* Set-up
* Differentiation
* Autocorrelation
* Partial Autocorrelation
* Model Choice: ARIMA(3,1,0)
* Fit Model
* Testing in Training Period
  + Metric 1: Correlation of Predicted and Actual Log Return
  + Metric 2: Precision, Recall, and Accuracy of Predicting Price Move Directions
* Testing in Cross-Validation Period
  + Metric 1: Correlation of Predicted and Actual Log Return
  + Metric 2: Precision, Recall, and Accuracy of Predicting Price Move Directions
* Comparison to Multivariate Rolling Regression

### 3. Logistic Regression Model for National Retail Gas Price Trend

* Set-up
* Binary Classification Problem
* Features
* Logistic Regression Path
* l2 Regularization Parameter
* Test in Cross-Validation Period
  + Prediction
  + Recall
  + Accuracy
* Comparison to Multivariate Rolling Regression and ARIMA

### 4. Saving Money from Predicting Los Angeles Gas Price Trend

* Set-up
* Correlation between National and Local Gas Price Move Direction
* Logistic Regression Model for Local Price Move
  * Features
  * Logistic Regression Path
  * l2 Regularization Parameter
* Test in Cross-Validation Period
  + Prediction
  + Recall
  + Accuracy
* How Much Money Can I Save?
  + Is it even possible to do much better?
