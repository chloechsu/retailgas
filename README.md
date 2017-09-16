# Weekly Retail Gas Price Prediction

Consider the following scenario. Suppose I drive about the same distance every
week and I have enough gas left in the tank for another week.
If I know the gas price is going down next week, I could save some money by
waiting till next week to fill up the tank.

With this motivation, it'd be nice to predict retail gas price trends. Compared
to crude oil, retail gas price changes more slowly (larger autocorrelation), so
it might be easier to predict than crude oil.

This project compares three models for predicting weekly trend of retail gas
prices:

[1. Multivariate Rolling Regression](multivariate_rolling_regression.html)
[2. ARIMA](ARIMA_model.html)
[3. Logistic Regression](logistic_regression.html)

(Please download the linked html files to view Jupyter notebooks.)

The predictors include: crude oil and gasoline spot prices, as well as crude oil
and gasoline stocks.
All data are from [U.S. Energy Information
Administration](https://www.eia.gov).

Model Comparison:

* Performance in Cross-Validation 

| Model                            | Precision   | Recall     | Accuracy  |
| -------------                    | ----------- | ---------- | --------- |
| Multivariate Rolling Regression  | 66%         |   78%      | 72%       |
| ARIMA                            | 68%         |   71%      | 72%       |
| Logistic Regression              | 91%         |   77%      | 86%       |

Under reasonable assumptions, an average driver would save about \$65 in
2011-2016 in Los Angeles.

## Table of Contents
### [1. Multivariate Rolling Regression Model for National Retail Gas Price](multivariate_rolling_regression.html)

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

### [2. ARIMA Model for National Retail Gas Price](ARIMA_model.html)

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

### [3. Logistic Regression Model for National Retail Gas Price Trend](logistic_regression.html)

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

### [4. Saving Money from Predicting Los Angeles Gas Price Trend](los_angeles.html)

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
