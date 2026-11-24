# Gold Price Analysis and Forecasting Using Time Series Models

## Project Overview
This project was completed as part of the Time Series and Forecasting Methods (SIT3005) course at Universiti Malaya.

The study investigates historical gold price movements, seasonal patterns, and short-term forecasting performance using time series analysis in R. It also examines gold price movements in relation to macroeconomic and geopolitical events.

## Objectives
- Analyze gold price movements from January to June 2022.
- Investigate trends and seasonality using historical data from 2018 to 2021.
- Examine public interest in gold using Google Trends.
- Forecast gold prices for the first 14 trading days of July 2022 using an ARIMA model.
- Evaluate forecasting performance by comparing predicted and actual prices.

## Tools and Technologies
- R
- RStudio
- R Markdown
- Google Trends

### R Packages
- ggplot2
- dplyr
- tsibble
- lubridate
- fpp3
- forecast

## Methodology

### 1. Data Cleaning and Preprocessing
- Converted date and price variables into appropriate data formats.
- Sorted observations in chronological order.
- Indexed observations by trading day to account for non-trading days.
- Aggregated historical daily prices into monthly average prices for seasonality analysis.

### 2. Exploratory Data Analysis
- Visualized historical gold price movements.
- Identified significant price fluctuations and market trends.
- Examined public search interest in gold using Google Trends.

### 3. Time Series Decomposition
Applied Seasonal-Trend Decomposition using LOESS (STL) to monthly gold prices from 2018 to 2021 to examine:
- Trend component
- Seasonal component
- Remainder component

### 4. Time Series Forecasting
- Training set: January–June 2022.
- Testing set: First 14 trading days of July 2022.
- Applied automatic ARIMA model selection using `auto.arima()`.
- Selected model: ARIMA(0,1,0) without drift.
- Generated forecasts with 80% and 95% prediction intervals.

### 5. Model Evaluation
Compared forecasted gold prices with actual observations using forecast accuracy metrics.

## Results and Key Findings

- Gold prices increased from approximately USD 1,800 to above USD 2,000 in early March 2022, coinciding with heightened geopolitical uncertainty.
- STL decomposition revealed weak and inconsistent seasonal effects.
- The selected ARIMA(0,1,0) model produced a constant point forecast of USD 1,807.30 per ounce.
- Actual gold prices declined during the testing period, while the model generally overestimated prices.
- Prediction intervals widened over the forecast horizon, reflecting increasing uncertainty.

### Forecast Accuracy

| Evaluation Metric | Result |
|---|---:|
| Mean Error (ME) | -73.7 |
| Root Mean Squared Error (RMSE) | 78.6 |
| Mean Absolute Error (MAE) | 73.7 |
| Mean Absolute Percentage Error (MAPE) | 4.28% |
| Residual Autocorrelation (ACF1) | 0.561 |

## Conclusion

The analysis identified weak seasonality and considerable short-term volatility in gold prices. The ARIMA model achieved a MAPE of 4.28%, but its tendency to overpredict prices and the remaining autocorrelation indicate limitations in capturing short-term price dynamics.

The findings highlight the importance of considering macroeconomic factors, geopolitical uncertainty, and forecasting limitations when analyzing financial time series.

## Skills Demonstrated
- Data cleaning and preprocessing
- Exploratory data analysis
- Statistical data visualization
- Time series decomposition
- ARIMA modeling and forecasting
- Model performance evaluation
- Statistical interpretation and reporting

## Repository Contents
- R Markdown report (PDF)
- Project poster (PDF)
- Historical gold price datasets (CSV)

## Academic Information
- Institution: Universiti Malaya
- Programme: Bachelor of Science in Statistics
- Course: SIT3005 – Time Series and Forecasting Methods
- Project type: Individual academic assignment
