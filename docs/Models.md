## Supported models

- kontrola accuracy and robustness of the models using cross-validation
- using [StatsForecast](https://nixtla.github.io/statsforecast/) we can train many models efficiently such as [AutoARIMA](https://fvigh.github.io/dipl/Models/#autoarima), AutoETS 

### Prophet
Facebook Prophet is an open-source library for univariate time series forecasting. It implements a procedure for forecasting time series data based on
an additive model where non-linear trends are fit with yearly, weekly, and daily seasonality, plus holiday effects. It works best with time series
that have strong seasonal effects and several seasons of historical data. Prophet is robust to missing data and shifts in the trend, and typically handles outliers well. [^1]

!!! info "Model info"
    $y(t) = g(t) + s(t) + h(t) + e(t)$

    Prophet features a decomposable time series with four components[^2]: growth (or trend) g(t), seasonality s(t), holidays h(t) (if present) and error term (e).    
    
### AutoARIMA
ARIMA is one of the most widely used models for time series forecasting. It was developed by Hyndman and Khandakar and from its conception has been an industry standard for its speed and accuracy. ARIMA models the time series through three parameters: the number of autoregressive terms $p$, the number of differences $d$, and the number of moving average parameters $q$. AutoARIMA finds the best ARIMA model; in this sense, the hyperparameter tuning (the right set of $p$,$d$,$q$) occurs inside the model using the Hyndman and Khandakar algorithm, so the user does not have to think about this task. The model focuses on leveraging autocorrelations to obtain accurate predictions and constitutes a well-proven model that works great for baselines.

!!! info "Model info"
    Automatically selected ARIMA model using Information Criterion (AICc).[^3]



*[ARIMA]: AutoRegressive Integrated Moving Average

[^1]: Prophet R Reference Material [link](https://cran.r-project.org/web/packages/prophet/prophet.pdf)

[^2]: Comparing Prophet and Deep Learning to ARIMA in Forecasting Wholesale Food Prices [link](https://browse.arxiv.org/pdf/2107.12770.pdf)

[^3]:
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.

