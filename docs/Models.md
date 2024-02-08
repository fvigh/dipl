## Podporované modely:
- [AutoARIMA](https://fvigh.github.io/dipl/Models/#autoarima)
- [AutoETS](https://fvigh.github.io/dipl/Models/#autoets)
- [AutoTheta](https://fvigh.github.io/dipl/Models/#autotheta)
- [Benchmark](https://fvigh.github.io/dipl/Models/#benchmark)


### AutoARIMA
Model sa zameriava na využitie autokorelácií na získanie presných predpovedí a predstavuje osvedčený model, ktorý skvele funguje ako referenčný model.

!!! info
    ARIMA modeluje časový rad pomocou troch parametrov: počet autoregresných členov $p$, počet diferencií $d$ a počet parametrov kĺzavého priemeru $q$. AutoARIMA nájde najlepší model ARIMA s pomocou AICc; ladenie hyperparametrov (správna množina $p$,$d$,$q$) prebieha vnútri modelu pomocou Hyndmanovho a Khandakarovho algoritmu. [^1]

### AutoETS
Automaticky vyberie najlepší model ETS (Error, Trend, Seasonality) pomocou Akaikeho informačného kritéria (AICc)

### AutoTheta
Automaticky vyberie najlepší model Theta (štandardný model Theta ("STM"), optimalizovaný model Theta ("OTM"), dynamický štandardný model Theta ("DSTM"), dynamický optimalizovaný model Theta ("DOTM")) pomocou MSE.

## Benchmark
Klasické modely na stanovenie referenčných hodnôt

### SeasonalNaive
Všetky predpovede majú hodnotu posledného pozorovania. Používa posledné známe pozorovanie z rovnakého obdobia (napr. z rovnakého mesiaca predchádzajúceho roka), aby sa zachytili sezónne výkyvy.

### HistoricAverage
Známa aj ako priemerná hodnota. Používa jednoduchý priemer všetkých minulých pozorovaní.

### RandomWalkWithDrift
Predpovedá budúce hodnoty na základe poslednej pozorovanej hodnoty upravenej o konštantný drift (trend).



*[ARIMA]: AutoRegressive Integrated Moving Average

[^1]: AutoARIMA [link](https://www.anyscale.com/blog/how-nixtla-uses-ray-to-accurately-predict-more-than-a-million-time-series)

