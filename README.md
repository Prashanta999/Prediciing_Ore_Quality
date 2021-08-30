# Predicting_Ore_Quality

## Goal

- To predict final % concentrate of iron (ore) or silica (waste) ahead of time using time-series analysis which will help engineers to maximize recovery while miniming tailings and decreasing costs. 
- Flotation processes can take 20-40 hours. Being able to predict the final product before the process starts allows for feed-forward optimization.

## Dataset

The Data set can be found on Kaggle at:
https://www.kaggle.com/edumagalhaes/quality-prediction-in-a-mining-process

The biggest takeway from analyzing this dataset is that the data is colleted at differnt intervals for different columns. For example, % Iron feed, % Silica Feed, % Iron Concentrate and % Silica Concentrate are collected every hour where as the other "process variables" are collected every 20 seconds. This poses an issue for time series analysis as we require each line in the dataset to be be a unique time. To solve this issue I took the average of the values so each line in the dataset corresponds to one hour increments. 

This updated dataset can be found here: https://github.com/Prashanta999/Prediciing_Ore_Quality/blob/main/Data_grouped_by_date.csv

##


##


 


