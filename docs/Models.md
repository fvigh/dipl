## Podporované modely
- [AutoARIMA](https://fvigh.github.io/dipl/Models/#autoarima)
- Prophet
- základné modely (Naive, Random)
- kontrola accuracy and robustness of the models using cross-validation

### Prophet
Facebook Prophet is an open-source library for univariate time series forecasting. It implements a procedure for forecasting time series data based on
an additive model where non-linear trends are fit with yearly, weekly, and daily seasonality, plus holiday effects. It works best with time series
that have strong seasonal effects and several seasons of historical data. Prophet is robust to missing data and shifts in the trend, and typically handles outliers well.

!!! info "Model info"
    $y(t) = g(t) + s(t) + h(t) + e(t)$

    Prophet features a decomposable time series with four components[^1]: growth (or trend) g(t), seasonality s(t), holidays h(t) (if present) and error term (e).    
    
### AutoARIMA
ARIMA modeluje časový rad pomocou troch parametrov: počet autoregresných členov $p$, počet diferencií $d$ a počet parametrov kĺzavého priemeru $q$. AutoARIMA nájde najlepší model ARIMA; ladenie hyperparametrov (správna množina $p$,$d$,$q$) prebieha vnútri modelu pomocou Hyndmanovho a Khandakarovho algoritmu, takže používateľ nemusí nad touto úlohou premýšľať. Model sa zameriava na využitie autokorelácií na získanie presných predpovedí a predstavuje osvedčený model, ktorý skvele funguje pre základné hodnoty.

ARIMA models the time series through three parameters: the number of autoregressive terms $p$, the number of differences $d$, and the number of moving average parameters $q$. AutoARIMA finds the best ARIMA model; the hyperparameter tuning (the right set of $p$,$d$,$q$) occurs inside the model using the Hyndman and Khandakar algorithm, so the user does not have to think about this task. The model focuses on leveraging autocorrelations to obtain accurate predictions and constitutes a well-proven model that works great for baselines. [^2]

!!! info "Model info"
    Automatically selected ARIMA model using Information Criterion (AICc).[^3]



*[ARIMA]: AutoRegressive Integrated Moving Average

[^1]: Comparing Prophet and Deep Learning to ARIMA in Forecasting Wholesale Food Prices [link](https://browse.arxiv.org/pdf/2107.12770.pdf)

[^2]: AutoARIMA [link](https://www.anyscale.com/blog/how-nixtla-uses-ray-to-accurately-predict-more-than-a-million-time-series)

[^3]:
    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod
    nulla. Curabitur feugiat, tortor non consequat finibus, justo purus auctor
    massa, nec semper lorem quam in massa.

