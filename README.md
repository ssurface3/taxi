# taxi
## Table of contents
* [General info](#general-info)
* [Features](#features)
* [Process](#process)
* [Stack](#stack)
* [Conclusion](#conclusion)

## General info
People really want to know, when to increase the supply of taxis on order to fight the price
## Features
* target - num_orders
* year
* month
* day
* Lags from 1 to 24 - to indicate the hour of a day
* rolling_mean 
## Process
|Stage | Description|
|--------|--------|
|First stage| Data preprocessing: removing Nans and giving data a good (and right) look|
|Second stage|Data analysis, mostly, graphs for lags determination|
|Third stage| Models training|
|Fourth stage| Model test on test sample for the best hyperparameters|
## Stack
Project is created with:
* Pandas
* Numpy
* statsmodel
* seaborn
* Sklearn
  1. Model_selection train_test_split
    1. RandomizedSearchCV
    2. TimeSeriesSplit
  2. sklearn.linear_model.LinearRegression
  3. sklearn.ensemble.RandomForestRegressor
  4. sklaern.tree.DecisionTreeRegressor
  5. AdaBoost and GradientBoost
  6. sklearn.preprocessing.StandardScaler
* pandas_profiling
* PCA(wasn't neede but i've tried)
* pipelines(same here)
* matplotlib.pyplot
* lgbm 
## Conclusion
* Found that the best hour for taxi is when other means of transport doesn't work
* Model show great results for guessing the number of orders throught the day
