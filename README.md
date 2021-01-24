# Sales Demand Forecast

- Data Source: Kaggle - Store Item Demand Forecasting Challenge (https://www.kaggle.com/c/demand-forecasting-kernels-only/data)

- The data contains of 5 years of store-item sales data, size 913000x4. Specifically, there are four columns:
    - Date (Ranges from 2013-01-01 to 2017-12-31)
    - Store (ID number of stores, ranges from 1-10)
    - Item (ID number of items, ranges from 1-50)
    - Sales (quantity sold)

- For this project, an ARIMA model is developed for prediction. Procedures below were followed:
    - Preparation of the data. Setting time as index
    - Data exploration to check potential pattern, such as trend or seasonality
    - Check stationarity of the data
        - Use ACF and PACF plots to check mean, variance and covariance
        - Use test_stationarity function to check test statistic and p-value
        - Apply differencing to achieve data stationarity
    - Use ACF and PACF plots to determine parameters for ARIMA model
        - Estimate the p, d, q values
        - Calculate the statistics for residuals and adjust the model accordingly
    - Use the built model for prediction
    