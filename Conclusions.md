# **Conclusions**

## Time-Series Forecasting

### *1) Based on your time series analysis, would you buy the yen now?*

The results of the time series analysis forecasts that the price of the yen is likely to rise over the next 5 days. 

###### **5-Day Yen Price Forecast**:
![5-day Yen Price Forecast](/Users/nsgolthi/Desktop/fintech_bc/Homework/assignment6_time_series/Time-Series/Images/5day_yen_price_fcst.png)

At the same time, the volatility forecast produced by the GARCH model suggests that the price of the yen will be increasingly volatile over the same period. 

###### **5-Day Yen Volatility Forecast**:
![5-day Yen Volatility Forecast](/Users/nsgolthi/Desktop/fintech_bc/Homework/assignment6_time_series/Time-Series/Images/5day_yen_vol_fcst.png)

With all of that considered, this would be a good opportunity to buy the yen given the forecasted price appreciation, particularly if a prospective investor is comfortable with risk. 

### *2) Is the risk of the yen expected to increase or decrease?*

Per the volatility forecast produced by the GARCH model, the risk of the yen is expected to increase over the next 5 days.

### *3) Based on the model evaluation, would you feel confident in using these models for trading?*
I would not be comfortable using the ARMA and ARIMA models for forecasting future returns. Both models have p-values that are significantly higher than the acceptable threshold of 0.05 (0.421 & 0.652, respectively). 

###### **ARMA Model Results**:
![ARMA Model Results](/Users/nsgolthi/Desktop/fintech_bc/Homework/assignment6_time_series/Time-Series/Images/ARMA_model_results.png)

###### **ARIMA Model Results**:
![ARIMA Model Results](/Users/nsgolthi/Desktop/fintech_bc/Homework/assignment6_time_series/Time-Series/Images/ARIMA_model_results.png)

As a result, I would likely need to adjust the lags used to improve the model results before using either model to provide actionable trading insight.

The GARCH model, on the other hand, does have a p-value below the accepted threshold of 0.05. 

###### **GARCH Model Results**:
![ARIMA Model Results](/Users/nsgolthi/Desktop/fintech_bc/Homework/assignment6_time_series/Time-Series/Images/GARCH_model_results.png)

This suggests that the AR lags and ARCH terms selected for the model are significant, and that the model will likely produce relatively sound forecasts. 

## Linear Regression Forecasting

### *Does this model perform better or worse on out-of-sample data compared to in-sample data?*

The linear regression model appears to perform better on the out-of-sample data than the in-sample data; the in-sample RMSE (0.596) is higher than the out-of-sample RMSE (0.415).

###### **In-Sample RMSE**:
![ARIMA Model Results](/Users/nsgolthi/Desktop/fintech_bc/Homework/assignment6_time_series/Time-Series/Images/in_RMSE.png)

###### **Out-of-Sample RMSE**:
![ARIMA Model Results](/Users/nsgolthi/Desktop/fintech_bc/Homework/assignment6_time_series/Time-Series/Images/out_RMSE.png)

To address these unexpected results, I believe we should consider expanding our pool of sample data. By using more data, it is likely that our in-sample performance increases. 