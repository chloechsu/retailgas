# Weekly Retail Gas Price Prediction

Predictive model for weekly retail gas prices in different states and cities.

Predictors: crude oil and gasoline spot prices, stocks, and supplies.

Data source: [U.S. Energy Information Administration](https://www.eia.gov)

The goal is to predict the **trend** of retail gas price, in order to save money
on gas.

Model Comparison:
* Performance in Cross-Validation 
| Model                            | Precision   | Recall     | Accuracy  |
| -------------                    |:-----------:|:----------:|:---------:|
| Multivariate Rolling Regression  | 66%         |   78%      | 72%       |
| ARIMA                            | 68%         |   71%      | 72%       |
| Logistic Regression              | 91%         |   77%      | 86%       |

Under reasonable assumptions, an average driver would save about \$65 in
2011-2016 in Los Angeles.

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
* Test in Cross-Validation Period
  + Metric 1: Correlation of Predicted and Actual Log Return
  + Metric 2: Prediction of Price Trend 

### 2. ARIMA Model for National Retail Gas Price

* Set-up
* Differentiation
* Autocorrelation
* Partial Autocorrelation
* Model Choice: ARIMA(3,1,0)
* Fit Model
* Test in Cross-Validation Period
  + Metric 1: Correlation of Predicted and Actual Log Return
  + Metric 2: Prediction of Price Trend 
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
