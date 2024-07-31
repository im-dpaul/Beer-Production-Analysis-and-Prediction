# Brewed Insights: Forecasting Monthly Beer Production

Time series analysis is a powerful tool for understanding and forecasting temporal data. This project involves the analysis and prediction of monthly beer production using various time series forecasting techniques including [SARIMA](https://en.wikipedia.org/wiki/Autoregressive_integrated_moving_average), [LSTM(RNN)](https://en.wikipedia.org/wiki/Long_short-term_memory) and [Prophet](https://facebook.github.io/prophet/) models. The goal is to explore the data, understand its patterns, and apply forecasting models to predict future beer production.

### About Data:
The dataset used in this project contains monthly beer production figures. It includes the following columns:
- `Month`: The month of production.
- `Monthly beer production`: The quantity of beer produced in that month.

### Table of Contents:
1. [Importing Libraries](#importing-libraries)
2. [Data Preprocessing](#data-preprocessing)
4. [Data Exploration and Visualization](#data-exploration-and-visualization)
5. [SARIMA Forecasting](#sarima-forecasting)
6. [LSTM (RNN) Forecasting](#lstm-rnn-forecasting)
7. [Prophet Forecasting](#prophet-forecasting)
8. [Model Comparison](#model-comparison)
9. [Conclusion](#conclusion)

## Importing Libraries
- `Pandas` & `NumPy` for data manipulation and analysis.
- `Matplotlib` & `Seaborn` for data visualization, creating plots and charts.
- `seasonal_decompose` & `SARIMAX` from `statsmodels` to explore & forecast time series data.
- `MinMaxScaler` from `sklearn` to scale model input data.
- `Sequential`, `Dense` & `LSTM` from `keras` for building LSTM(RNN) model.
- `Prophet` from `prophet` library for time series forcasting.
- `mean_squared_error` & `rmse` from `sklearn` & `statsmodels` to evaluate model performance.

## Data Preprocessing
- **Loading the Data**: The dataset is loaded into a Pandas DataFrame.
- **Date Conversion**: The `Month` column is converted to a datetime object and set as the index.
- **Frequency Setting**: The frequency of the datetime index is set to monthly (`'MS'`).

## Data Exploration and Visualization
- **Basic Information**: The structure and summary statistics of the data are explored.
- **Seasonality**: Plot the monthly beer production to visualize the overall trend and seasonal patterns in the data.
- **Seasonal Decomposition**: The `seasonal_decompose` function is used to decompose the time series into its trend, seasonal and residual components using the additive model to better understand the underlying patterns.

## SARIMA Forecasting
- **SARIMA Model**: A Seasonal ARIMA (SARIMA) model to forecast future production based on past trends and seasonality.
- **Model Fitting**: A SARIMA model is fitted to the training data.
- **Prediction**: The model predicts beer production for the test period.
- **Evaluation**: The predictions are evaluated using RMSE and MSE metrics.

## LSTM (RNN) Forecasting
- **LSTM Model**: A Long Short-Term Memory (LSTM) model, a type of Recurrent Neural Network (RNN), for time series forecasting.
- **Data Scaling**: The data is scaled using `MinMaxScaler`.
- **Model Building**: An LSTM model is built and trained on the scaled data.
- **Prediction**: The model predicts beer production for the test period.
- **Evaluation**: The predictions are evaluated using RMSE and MSE metrics.

## Prophet Forecasting
- **Prophet Model**: Facebook's Prophet library, a versatile forecasting tool, to predict future production.
- **Model Fitting**: Trains the model on historical data and generates forecasts for upcoming months.
- **Prediction**: The model predicts beer production for the test period.
- **Evaluation**: The predictions are evaluated using RMSE and MSE metrics.

## Model Comparison
- The performance of all three forecasting models (SARIMA, LSTM, Prophet) is compared using on RMSE and MSE metrics.
- Provides a table summarizing the error metrics for each model.
- Visualizes all predictions along with the actual production data for a comprehensive comparison.

## Conclusion
This project demonstrates the power of time series analysis for uncovering patterns and predicting future trends in time-dependent data. By leveraging various forecasting techniques, valuable insights can be gained for informed decision-making within the beer production industry.
