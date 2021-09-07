# Predicting Ore Quality (Proof of Concept)

**Author: Prashanta Saha**

## Goal

- To predict final % concentrate of iron (ore) or silica (waste) ahead of time using machine learning & time-series analysis which will help engineers to maximize recovery while minimizing tailings and decreasing costs. 

- Flotation processes can take 20-40 hours. Being able to predict the final product before the process starts allows for feed-forward optimization.

## Dataset

- The Data set can be found on Kaggle at:
https://www.kaggle.com/edumagalhaes/quality-prediction-in-a-mining-process

- Data Gathering & EDA can be found here: https://github.com/Prashanta999/Prediciing_Ore_Quality/blob/main/Data%20Gathering%20%26%20EDA.ipynb

- The biggest takeaway from analyzing this dataset is that the data is collected at different intervals for different columns. For example, % Iron feed, % Silica Feed, % Iron Concentrate and % Silica Concentrate are collected every hour whereas the other "process variables" are collected every 20 seconds. This poses an issue for time series analysis as we require each line in the dataset to be a unique time. To solve this issue I took the average of the values so each line in the dataset corresponds to one hour increments. This, however, significantly reduces the size of the originally dataset by 180x.

- This updated dataset can be found here: https://github.com/Prashanta999/Prediciing_Ore_Quality/blob/main/Data_grouped_by_date.csv

## Machine Learning (Regression Models)

- Before doing time series analysis I wanted to see how accurate the data was at predicting % concentrate iron and % concentrate silica using ML methods

- I used ML techniques like Random Forest, XGBoost, Support Vector Machine, etc for the modelling 

- I removed the date column for these models

- The file for the modelling can be found here: https://github.com/Prashanta999/Prediciing_Ore_Quality/blob/main/Regression%20Modeling.ipynb

## PCA + Machine Learning (Regression Models)

- I also tested how dimensionality reduction could help in predicting the models

- The file for the modelling can be found here: https://github.com/Prashanta999/Prediciing_Ore_Quality/blob/main/PCA.ipynb

- PCA doesn't provide any valuable insights for our models. This maybe due to the poor corrleations between the target and normal variables

## Time Series Analysis

- The file for the modelling can be found here: https://github.com/Prashanta999/Prediciing_Ore_Quality/blob/main/Time_Series_Analysis.ipynb

- The time series analysis was done on google collab

- My procedure for time series modelling involved firstly decomposing the the dataset in order to better understand any trend, seasonality or noise components in the model. The target variable was found to be stationary which allowed for MA and ARIMA to be created as baseline models. This was followed by LSTM model using multiple time steps and a 1D CNN model for time series

- Time series provided the best results for prediciting "% Silica Concentrate" & "% Iron Concentrate"

 


