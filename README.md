# xtutest 1.3.0

Test for an inverse U-shaped (or U-shaped) relationship and estimate its turning point in heterogeneous
panels with cross-sectional dependence, for Stata 14 or later.

* CCE mean-group unit regressions (Pesaran 2006) of y on x, x^2 and controls
* Lind-Mehlum (2010) intersection-union test on an interval [xL, xH], t(N-1) or normal reference
* turning point of the mean curve with Fieller and delta intervals; median unit turning point
* balanced or unbalanced panels
* Pesaran CD test; pooled two-way fixed-effects comparison; graphs
* `estimator(ccep)`: CCE pooled (common slopes, robust to cross-sectional dependence)
* `estimator(fe|re|iv|gmm)`: homogeneous-slope variants (comparisons and robustness checks)
* residual diagnostics for every estimator: serial correlation, heteroskedasticity, normality, stability

```stata
net install xtutest, from("C:/path/to/xtutest") replace
net get xtutest, from("C:/path/to/xtutest")      // example dataset xtutest_apec.dta
help xtutest
use xtutest_apec, clear
xtset id year
gen lnEF = ln(EF)
xtutest lnEF NET GLB, pooled
```

Author: Yusuf Toyin Yusuf, Kwara State University (yusuf.yusuf@kwasu.edu.ng). Licence: MIT.
