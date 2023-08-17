# USD-INR-currency-exchange-rate-forecasting
The code provided is  analysis of the USD - INR (US Dollar to Indian Rupee) exchange rate data using Python and various data analysis and time series forecasting techniques. The code is structured into several sections, each focusing on different aspects of data preprocessing, exploratory data analysis (EDA), time series decomposition, forecasting, and evaluation.

## Data Loading and Initial Analysis:
The code begins by importing necessary libraries, such as pandas, numpy, matplotlib, seaborn, and plotly, and loads the exchange rate data from a CSV file named "INR-USD.csv" using pandas' read_csv function. The .head() method is used to display the initial rows of the dataset.

## Data Cleaning:
The code checks for missing values using isnull().sum() and removes rows with missing values using the dropna() function.

## Descriptive Statistics and Time Transformations:
Descriptive statistics are computed using describe(). The code then converts the "Date" column to datetime format and extracts year and month information into separate columns. The data is visualized using Plotly Express and a line plot depicting the USD - INR conversion rate over the years is displayed.

## Yearly and Monthly Growth Analysis:
The code calculates the yearly growth of the exchange rate using percentage change. It uses Plotly to visualize the yearly growth rates in a bar plot. Monthly growth rates are calculated and averaged, and a bar plot is generated to show the aggregated monthly growth rates.

## Stationarity Test and Differencing:
The Augmented Dickey-Fuller test is performed to check the stationarity of the time series data. The data is then differenced using the seasonal difference, and another stationarity test is conducted.

## Autocorrelation and Partial Autocorrelation Analysis:
Autocorrelation and partial autocorrelation plots are generated using the plot_acf and plot_pacf functions from the statsmodels.graphics.tsaplots module.

## Seasonal Decomposition and Visualization:
Seasonal decomposition of the time series data is performed using the seasonal_decompose function from statsmodels.tsa.seasonal. The trend, seasonal, and residual components are plotted using Matplotlib.

## Time Series Forecasting:
The code utilizes the auto_arima function from pmdarima.arima to automatically determine the optimal ARIMA model order for the data. The SARIMAX model is then fit to the data using the selected order parameters. The model summary is printed.

## Forecast Evaluation:
The code calculates the Mean Absolute Error (MAE) and Mean Absolute Percentage Error (MAPE) for the predictions made by the SARIMAX model. The predictions are visualized using Plotly to compare them against the training data.

## Final Forecast Visualization:
The SARIMAX model is used to make predictions for the last 200 data points, and the MAE and MAPE are calculated again. The final predictions and training data are visualized using Plotly to provide an overview of the model's performance.

