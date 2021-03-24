# Time Series Analysis and Forecasting


## Components of Time Series:
- Trend
- Seasonality
- Autocorrelation
- Noise
- Irregularity
- Cyclic


## Stationary Data:

![time_series](time series.png)

When a time series is stationary, it can be easier to model. Statistical modeling methods assume or require the time series to be stationary.

There are multiple tests that can be used to check stationarity.

- ADF( Augmented Dicky Fuller Test)
- KPSS
- PP (Phillips-Perron test)

## Statistical significance - p-values
The testing part of hypothesis tests allows us to determine which theory, the null or alternative, is better supported by the evidence. 

The level of significance(alpha) is the percentage of risk we are willing to take while rejecting the null hypothesis.
P-value is the probability that a random chance generated the data or something else that is equal or rarer (under the null hypothesis). We calculate the p-value for the sample statistics(which is the sample mean in our case). We can do it manually by looking at the z-table or use some statistical software to compute it.


## The ARIMA Time Series Model
One of the most common methods used in time series forecasting is known as the ARIMA model, which stands for AutoregRessive Integrated Moving Average. ARIMA is a model that can be fitted to time series data in order to better understand or predict future points in the series.

There are three distinct integers (p, d, q) that are used to parametrize ARIMA models. Because of that, ARIMA models are denoted with the notation ARIMA(p, d, q). Together these three parameters account for seasonality, trend, and noise in datasets:

**p**: is the *auto-regressive* part of the model. It allows us to incorporate the effect of past values into our model. Intuitively, this would be similar to stating that it is likely to be warm tomorrow if it has been warm the past 3 days.

**d**: is the *integrated* part of the model. This includes terms in the model that incorporate the amount of differencing (i.e. the number of past time points to subtract from the current value) to apply to the time series. Intuitively, this would be similar to stating that it is likely to be same temperature tomorrow if the difference in temperature in the last three days has been very small.

**q**: is the *moving average* part of the model. This allows us to set the error of our model as a linear combination of the error values observed at previous time points in the past.

When dealing with seasonal effects, we make use of the seasonal ARIMA, which is denoted as ARIMA(p,d,q)(P,D,Q)s. Here, (p, d, q) are the non-seasonal parameters described above, while (P, D, Q) follow the same definition but are applied to the seasonal component of the time series. The term s is the periodicity of the time series (4 for quarterly periods, 12 for yearly periods, etc.)


**Trailing Vs Centered windows**

`Forecasts = trailing moving avergae of differenced series + centered moving average of past series (t-365)`

References:
https://www.khanacademy.org/math/statistics-probability
