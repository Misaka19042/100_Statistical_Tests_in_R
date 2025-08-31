# Statistical Tests and R Datasets Mapping

| Test \# | Test Name | Recommended Dataset(s) | Variables/Usage |
|----|----|----|----|
| 1 | Pearson's correlation t-test | iris, mtcars | Sepal.Length \~ Petal.Length; mpg \~ wt |
| 2 | Spearman rank correlation | iris, mtcars | Same as above for non-parametric |
| 3 | Kendall's tau correlation | iris, mtcars | Same as above for ordinal data |
| 4 | Z test difference between correlations | iris | Compare correlations across species |
| 5 | Difference between overlapping correlations | mtcars | mpg\~wt vs mpg\~hp with shared mpg |
| 6 | Difference between non-overlapping correlations | mtcars | mpg\~wt vs hp\~qsec |
| 7 | Bartlett's test of sphericity | iris[,1:4] | Test correlation matrix |
| 8 | Jennrich test equality of matrices | iris | Compare correlation matrices by species |
| 9 | Granger causality | AirPassengers, lynx | Time series causality |
| 10 | Durbin-Watson autocorrelation | airquality | Residuals from lm(Ozone \~ Temp) |
| 11 | Breusch-Godfrey autocorrelation | airquality | Same model as above |
| 12 | One sample t-test | iris | Test if mean Sepal.Length = 5.8 |
| 13 | One sample Wilcoxon | iris | Non-parametric version of above |
| 14 | Sign test for median | iris | Test median Sepal.Length |
| 15 | Two sample t-test | iris | Compare setosa vs versicolor |
| 16 | Pairwise t-test | iris | All species comparisons |
| 17 | Pairwise t-test common variance | iris | Same with pooled variance |
| 18 | Welch t-test | iris | Unequal variance t-test |
| 19 | Paired t-test | sleep | extra \~ group (paired by ID) |
| 20 | Matched pairs Wilcoxon | sleep | Non-parametric paired test |
| 21 | Pairwise paired t-test | sleep | Multiple paired comparisons |
| 22 | Pairwise Wilcox test | iris | Non-parametric pairwise |
| 23 | Two sample dependent sign rank | sleep | Alternative paired test |
| 24 | Wilcoxon rank sum | iris | Non-parametric two-sample |
| 25 | Wald-Wolfowitz runs (dichotomous) | Generate binary sequence | Test randomness |
| 26 | Wald-Wolfowitz runs (continuous) | faithful$eruptions | Test randomness |
| 27 | Bartels test randomness | faithful$eruptions | Alternative randomness test |
| 28 | Ljung-Box test | AirPassengers residuals | Test autocorrelation |
| 29 | Box-Pierce test | AirPassengers residuals | Alternative to Ljung-Box |
| 30 | BDS test | lynx or stock returns | Test independence |
| 31 | Wald-Wolfowitz two sample | iris | Test if two samples differ |
| 32 | Mood's test | iris | Test scale differences |
| 33 | F-test equality of variances | iris | Compare setosa vs versicolor variance |
| 34 | Pitman-Morgan test | sleep | Test paired variance equality |
| 35 | Ansari-Bradley test | iris | Non-parametric variance test |
| 36 | Bartlett test homogeneity | iris | Test variance across all species |
| 37 | Fligner-Killeen test | iris | Non-parametric Bartlett |
| 38 | Levene's test | iris | Robust variance test |
| 39 | Cochran C test | iris | Test outlying variance |
| 40 | Brown-Forsythe test | iris | Modified Levene's test |
| 41 | Mauchly's sphericity | iris (repeated measures) | Test sphericity assumption |
| 42 | Binomial test | Generate binary data | Test proportion = 0.5 |
| 43 | One sample proportions | UCBAdmissions | Test admission rate |
| 44 | One sample Poisson | discoveries | Test rate parameter |
| 45 | Pairwise proportions | UCBAdmissions | Compare departments |
| 46 | Two sample Poisson | discoveries (split) | Compare rates |
| 47 | Multiple proportions | UCBAdmissions | Test all departments |
| 48 | Chi-squared linear trend | UCBAdmissions | Test trend in proportions |
| 49 | Paired chi-squared | UCBAdmissions | Paired categorical test |
| 50 | Fisher's exact test | UCBAdmissions (2x2) | Small sample categorical |
| 51 | Cochran-Mantel-Haenszel | UCBAdmissions | Stratified analysis |
| 52 | McNemar's test | Generate paired binary | Paired categorical data |
| 53 | One-way ANOVA | iris | Compare means across species |
| 54 | Welch ANOVA | iris | ANOVA with unequal variances |
| 55 | Kruskal-Wallis | iris | Non-parametric ANOVA |
| 56 | Friedman's test | iris (restructured) | Repeated measures non-parametric |
| 57 | Quade test | iris (restructured) | Alternative to Friedman |
| 58 | D'Agostino skewness | iris, faithful | Test skewness |
| 59 | Anscombe-Glynn kurtosis | iris, faithful | Test kurtosis |
| 60 | Bonett-Seier kurtosis | iris, faithful | Alternative kurtosis test |
| 61 | Shapiro-Wilk | iris$Sepal.Length | Test normality |
| 62 | Kolmogorov-Smirnov normality | iris$Sepal.Length | Alternative normality test |
| 63 | Jarque-Bera | iris$Sepal.Length | Joint skew/kurtosis test |
| 64 | D'Agostino omnibus | iris$Sepal.Length | Combined normality test |
| 65 | Anderson-Darling normality | iris$Sepal.Length | Sensitive normality test |
| 66 | Cramer-von Mises | iris$Sepal.Length | Alternative to AD |
| 67 | Lilliefors | iris$Sepal.Length | KS with estimated parameters |
| 68 | Shapiro-Francia | iris$Sepal.Length | Alternative to Shapiro-Wilk |
| 69 | Mardia's multivariate | iris[,1:4] | Multivariate normality |
| 70 | KS goodness of fit | faithful$eruptions | Test specific distribution |
| 71 | AD goodness of fit | faithful$eruptions | Alternative to KS |
| 72 | Two-sample KS | iris (two species) | Compare distributions |
| 73 | AD multiple sample | iris (all species) | Compare multiple distributions |
| 74 | Brunner-Munzel | iris | Generalised Wilcoxon |
| 75 | Dixon's Q | iris with outlier | Detect single outlier |
| 76 | Chi-squared outliers | iris | Multivariate outliers |
| 77 | Bonferroni outlier | mtcars | Multiple outlier detection |
| 78 | Grubbs test | iris with outlier | Parametric outlier test |
| 79 | Goldfeld-Quandt | mtcars | Test heteroscedasticity |
| 80 | Breusch-Pagan | mtcars | Alternative heteroscedasticity |
| 81 | Harrison-McCabe | mtcars | Another heteroscedasticity test |
| 82 | Harvey-Collier | mtcars | Test linearity |
| 83 | Ramsey RESET | mtcars | Specification test |
| 84 | White neural network | mtcars | Non-linear specification |
| 85 | Augmented Dickey-Fuller | AirPassengers | Unit root test |
| 86 | Phillips-Perron | AirPassengers | Alternative unit root |
| 87 | Phillips-Ouliaris | AirPassengers, lynx | Cointegration test |
| 88 | KPSS | AirPassengers | Stationarity test |
| 89 | Elliott-Rothenberg-Stock | AirPassengers | Efficient unit root test |
| 90 | Schmidt-Phillips | AirPassengers | Another unit root test |
| 91 | Zivot-Andrews | AirPassengers | Unit root with break |
| 92 | Grambsch-Therneau | survival::lung | Test proportional hazards |
| 93 | Mantel-Haenszel log-rank | survival::lung | Compare survival curves |
| 94 | Peto and Peto | survival::lung | Modified log-rank |
| 95 | Kuiper's uniformity | circular::fisherB1 | Circular uniformity |
| 96 | Rao's spacing uniformity | circular::fisherB1 | Alternative circular test |
| 97 | Rayleigh uniformity | circular::fisherB1 | Test circular uniformity |
| 98 | Watson's goodness of fit | circular::fisherB1 | Circular distribution test |
| 99 | Watson's two-sample | circular::fisherB1 | Compare circular samples |
| 100 | Rao's homogeneity | circular::fisherB1 | Test circular homogeneity |
| 101 | Pearson Chi-square | UCBAdmissions, Titanic | General association test |

## Key Dataset Groups:

**Core R datasets (base):** - iris, mtcars, airquality, sleep, faithful, UCBAdmissions, Titanic, discoveries, lynx, AirPassengers

**Additional package requirements:** - survival: lung, ovarian - circular: fisherB1, wind - Various test packages: lmtest, tseries, nortest, car
