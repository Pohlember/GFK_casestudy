# GFK Airport Taxi Order Forecast

## Table of contents
* [General info](#general-info)
* [EDA](#eda)
* [Baseline-model](#Baseline-model)
* [Heuristic-model](#Heuristic-model)
* [Timeseries-model](#Timeseries-model)
* [Hybrid-model](#Hybrid-model)
* [SARIMAX-model](#SARIMAX-model)

## General info
The project exercise was to forecast hourly bookings on an hourly basis given the historical dataset. Use RMSE to evaluate model performance and the last 10% of the dataset as validation set.

The code itself can be found under Gfk_Case.ipynb while the dataset is under taxi.csv.

## EDA
Initial exploration of the dataset.

## Baseline-model
Model the trend of the dataset and use that as baseline score.

## Heuristic-model
Based on heuristics find new features with predictive power, build a baseline XGBRegressor model and evaluate feature importance in the dataset. 

## Timeseries-model
Next, explore Trend/Seasonal/Cyclical models by first analysing the time-dependent trend of the process, then a simple lag-based regression approach to finally spot 
seasonal elements using seasonal and fourier plots as well as find dependencies using ACF/PACF plots to create a TSC model.

## Hybrid-model
Combine the previous to approaches by stacking the model output of two models:
1) a linear regression capturing the trend of the series as well as faciliates forecasting to the future
2) an ensemble tree-based model to incorporate interaction terms as well as handle non-linearities in the ordinal variables

## SARIMAX-model
Lastly, explore a pure time series model building the model as a combination of autoregressive and moving average components. 
