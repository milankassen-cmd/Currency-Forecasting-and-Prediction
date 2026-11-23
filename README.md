<h1> Currency Forecasting and Prediction </h1>

<h2> Introduction </h2>
In this project I used advanced time series forecasting methods to model the data of the Rand to US Dollar exchange rate over a period of 12 months. Starting with a baseline ARIMA model to advanced ARIMA models and finally a machine learning approach using Linear Regression to see which model performs best on real data and which model can capture the trend and make the best prediction.

<h2> Objective </h2>
The objective of this project was to see how closely the models used would accurately predict the final close price of the exchange rate on an up-to-date basis. This type of forecasting techniques could be used across different industries with a strong time variable like the retail industry. 

<h2> Data and Packages </h2>
<b> Packages: </b> numpy, pandas, plotly, pmdarima, scikit-learn, statsmodels, yfinance <br>
<b> Data Source: </b> data obtained from the yfinance library

<h2> Data Cleaning and EDA </h2>
No EDA was needed for this project as the yfinance library provides real finance data that has been structured. There was minimal data cleaning need, only checking for missing values and then forward filling those values, this method is best used in time series projects as autoregressive models do not deal with missing values well and neither do other time series methods.

<h2> Conclusion </h2>
The ARIMA model is the baseline used and captures the data well but does not yield an accurate prediction/forecast. We use an advanced ARIMA model with an exogeneous variable (Dynamic Regression) - this models seems to perform the best as it uses the Low Price column as the extra variable in the time series and we see that it does not capture the train data as well but does make a more accurate prediction/forecast. The Dynamic Harmonic Regression model used captures the train data very well and probably overfits the data but then does not predict/forecast well - this makes sense as Harmonic Regression is used to capture seasonality which finance data does not really have. Lastly, is the Linear Regression model used for time series which does well with its forecast compared to the other models even though it fits the train data worse than the others - showcasing that machine learning methods are powerful. The data used is real data from the yfinance library and changes when the notebook is run and variability in model performance will be seen as finance data is quite volatile. In a production environment it would still be best to use traditional time series methods like the Dynamic Regression Model as the autocorrelation captures the train data well and most likely would be more consistent over a longer production period. Harmonic Regression Models would be good for seasonality in industries like retail where holidays are present and would impact sales and this is where machine learning methods would fall short for time series forecasting.
