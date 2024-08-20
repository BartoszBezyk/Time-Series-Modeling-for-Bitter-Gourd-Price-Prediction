# Time Series Modeling for Bitter Gourd Price Prediction

## Overview

This project focuses on predicting the price of Bitter Gourd using time series modeling techniques. The dataset spans from 2013 to 2021, containing daily price information for various fruits and vegetables. The goal is to develop an accurate predictive model that can forecast future prices based on historical data.

## Project Objectives

1. **Data Preparation**: 
   - Aggregate daily price data into monthly averages.
   - Clean the data by addressing missing values and outliers.
   - Adjust for calendar variations (e.g., differences in the number of days per month).

2. **Time Series Modeling**: 
   - Apply various time series models, including Moving Average (MA), Autoregressive (AR), and a combination of Trend + Seasonality + MA models, to forecast Bitter Gourd prices.
   - Use automatic model selection tools (`auto.arima`) and linear models (`tslm`) to find the best-fitting model.

3. **Model Evaluation**: 
   - Compare models based on key statistical metrics such as AICc, BIC, RMSE, MAE, and MAPE to identify the best-performing model.
   - Analyze the model's residuals and other diagnostic plots to ensure the assumptions of the models are satisfied.

4. **Prediction**: 
   - Use the best model to forecast future prices.
   - Assess the model's accuracy on a test set using metrics like RMSE and MAE.

## Tools and Libraries Used

- **R Programming Language**: The primary tool used for data processing, model building, and evaluation.
- **Libraries**:
  - `dplyr`: For data manipulation and preprocessing.
  - `lubridate`: For working with date-time data.
  - `zoo`: For handling irregular time series data.
  - `forecast`: For building and evaluating time series models, including ARIMA.
  - `stats`: Base R functions used for statistical calculations.
  - `knitr`: For creating dynamic reports and tables.

## Data Source

The [data](https://www.kaggle.com/datasets/mexwell/fruits-and-vegetables-price-dataset) was sourced from Kaggle, specifically from a dataset that includes daily prices for various fruits and vegetables over nine years (2013-2021). For this project, the focus was narrowed to Bitter Gourd.

## Methodology

1. **Data Aggregation**: Daily prices were aggregated to monthly averages to reduce noise and highlight longer-term trends.
2. **Data Cleaning**: Outliers were identified and adjusted, and missing values were handled to ensure the accuracy of the models.
3. **Model Building**: Several time series models were built, including:
   - MA(12) and MA(1) after differencing.
   - AR(1) and AR(9) models.
   - A combined model incorporating trend, seasonality, and MA components.
4. **Model Selection**: Models were compared based on AICc, BIC, RMSE, and other metrics to identify the best-performing model.
5. **Prediction and Validation**: The selected model was used to predict future prices, and its performance was validated on a holdout test set.

## Key Results

- The **AR(9)** model was identified as the best-performing model based on its low RMSE and favorable AICc and BIC values.
- The RMSE of the AR(9) model on the test set was 14.73, indicating a good fit relative to the range and mean of the data.

## Conclusion

This project successfully applied time series modeling techniques to predict the prices of Bitter Gourd. The AR(9) model was found to be the most effective, demonstrating the value of autoregressive models in capturing the underlying patterns in time series data. The methods and models used can be extended to other fruits and vegetables in the dataset for similar predictive analysis.
