## Podporované modely - kontrola accuracy and robustness of the models using cross-validation
- [AutoARIMA](https://fvigh.github.io/dipl/Models/#autoarima)
- [Prophet](https://fvigh.github.io/dipl/Models/#prophet)
- Benchmark: klasické modely na stanovenie referenčných hodnôt (Mean, Naive, Random Walk)


### AutoARIMA
Model sa zameriava na využitie autokorelácií na získanie presných predpovedí a predstavuje osvedčený model, ktorý skvele funguje ako referenčný model.

!!! info
    ARIMA modeluje časový rad pomocou troch parametrov: počet autoregresných členov $p$, počet diferencií $d$ a počet parametrov kĺzavého priemeru $q$. AutoARIMA nájde najlepší model ARIMA s pomocou AICc; ladenie hyperparametrov (správna množina $p$,$d$,$q$) prebieha vnútri modelu pomocou Hyndmanovho a Khandakarovho algoritmu. [^1]


### Prophet
Facebook Prophet is an open-source library for univariate time series forecasting. It implements a procedure for forecasting time series data based on
an additive model where non-linear trends are fit with yearly, weekly, and daily seasonality, plus holiday effects. It works best with time series
that have strong seasonal effects and several seasons of historical data. Prophet is robust to missing data and shifts in the trend, and typically handles outliers well.

!!! info "info"
    $y(t) = g(t) + s(t) + h(t) + e(t)$

    Prophet features a decomposable time series with four components[^2]: growth (or trend) g(t), seasonality s(t), holidays h(t) (if present) and error term (e).    
    

*[ARIMA]: AutoRegressive Integrated Moving Average

[^1]: AutoARIMA [link](https://www.anyscale.com/blog/how-nixtla-uses-ray-to-accurately-predict-more-than-a-million-time-series)

[^2]: Comparing Prophet and Deep Learning to ARIMA in Forecasting Wholesale Food Prices [link](https://browse.arxiv.org/pdf/2107.12770.pdf)
