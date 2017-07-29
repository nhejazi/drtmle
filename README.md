# R/`drtmle`

[![Travis-CI Build Status](https://travis-ci.org/benkeser/drtmle.svg?branch=master)](https://travis-ci.org/benkeser/drtmle)
[![AppVeyor Build  Status](https://ci.appveyor.com/api/projects/status/github/benkeser/drtmle?branch=master&svg=true)](https://ci.appveyor.com/project/benkeser/drtmle)
[![Coverage Status](https://img.shields.io/codecov/c/github/benkeser/drtmle/master.svg)](https://codecov.io/github/benkeser/drtmle?branch=master)
[![CRAN](http://www.r-pkg.org/badges/version/drtmle)](http://www.r-pkg.org/pkg/drtmle)
[![Project Status: Active - The project has reached a stable, usable state and is being actively developed.](http://www.repostatus.org/badges/latest/active.svg)](http://www.repostatus.org/#active)
[![MIT license](http://img.shields.io/badge/license-MIT-brightgreen.svg)](http://opensource.org/licenses/MIT)

> Doubly Robust, Asymptotically Linear Targeted Minimum Loss-Based Estimation 

---

## Description

`drtmle` is an R package that computes marginal effect estimators for binary 
treatments on continuous and binary outcomes. The TMLE estimators are doubly
robust, not only with respect to consistency, but also with respect to asymptotic 
normality, as discussed in Benkeser, Carone, van der Laan \& Gilbert, 2017,(_accepted Biometrika_, [working paper](http://biostats.bepress.com/ucbbiostat/paper356/)). 

---

## Installation

- Install the most recent _stable release_:
  `devtools::install_github("benkeser/drtmle")`

- To contribute, install the _development version_:
  `devtools::install_github("benkeser/drtmle", ref = "develop")`

---

## Use 

This package can be used to estimate covariate-adjusted marginal means under multiple discrete levels of a treatment. It may be used in situations where data consist of a vector of baseline covariates (`W`), a multi-level treatment assignment (`A`), and a continuous or binary-valued outcome (`Y`). The function `drtmle` may be used to estimate $E[E(Y | A=a_0, W)]$ for user-selected values of $a_0$ (via option `a_0`). The resulting targeted minimum loss-based estimates are doubly robust with respect to both consistency and asymptotic normality. The function computes doubly robust variance estimators that can be used to construct doubly robust confidence intervals for covariate-adjusted marginal means and contrasts between these means (via the `drconfint` function) for different levels of $a_0$. Doubly robust hypothesis tests are also available (via `drtest` function). A simple example on simulated data is shown below. 

```{r}

```


---

## License

&copy; 2016-2017 [David C. Benkeser](http://www.benkeserstatistics.com)

The contents of this repository are distributed under the MIT license. See
below for details:
```
The MIT License (MIT)

Copyright (c) 2016-2017 David C. Benkeser

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```