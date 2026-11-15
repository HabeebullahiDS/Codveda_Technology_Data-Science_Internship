# Level 3, Task 1: Time Series Analysis

**Codveda Technology | Data Science Internship**

## Objective
Analyse and forecast monthly airline passenger numbers.

## Dataset
`airline_passengers.csv`: 144 monthly records, 1949 to 1960 (passengers in thousands). The last 24 months were held out for testing.

## Approach
1. Plotted the series and decomposed it into trend, seasonality and residual (multiplicative).
2. Applied moving averages and checked stationarity (ADF test, ACF and PACF).
3. Forecast with a seasonal-naive baseline, Simple Exponential Smoothing, Holt-Winters and SARIMA.
4. Selected SARIMA(0,1,1)(0,1,1,12) by lowest AIC (-389.0) from 36 candidates.
5. Compared models by RMSE, MAE and MAPE on the test period.

## Key Results
| Model | RMSE |
|---|---|
| Holt-Winters | 32.49 |
| SARIMA | 43.17 |
| Seasonal naive | 76.99 |
| Simple smoothing | 137.33 |

- Average monthly passengers grew 276% from 1949 to 1960; July and August are the peak months.
- Holt-Winters had the lowest error (MAPE 6.4%); all forecasts fall below the actual 1960 peaks.
- The 1961 forecast averages about 520 thousand passengers per month.

## Files
- `Level3_Task1_Time_Series.ipynb`
- `airline_passengers.csv` (input)

## Libraries
pandas, numpy, matplotlib, statsmodels, scikit-learn
