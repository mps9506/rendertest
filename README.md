<!-- README.md is generated from README.Rmd. Please edit that file -->

rendertest
==========

<!-- badges: start -->

[![R build
status](https://github.com/mps9506/rendertest/workflows/R-CMD-check/badge.svg)](https://github.com/mps9506/rendertest/actions)
<!-- badges: end -->

The goal of rendertest is to …

Installation
------------

You can install the released version of rendertest from
[CRAN](https://CRAN.R-project.org) with:

    install.packages("rendertest")

And the development version from [GitHub](https://github.com/) with:

    # install.packages("devtools")
    devtools::install_github("mps9506/rendertest")

Example
-------

What is special about using `README.Rmd` instead of just `README.md`?
You can include R chunks like so:

    library(dplyr)
    #> 
    #> Attaching package: 'dplyr'
    #> The following objects are masked from 'package:stats':
    #> 
    #>     filter, lag
    #> The following objects are masked from 'package:base':
    #> 
    #>     intersect, setdiff, setequal, union
    head(tibble::as_tibble(cars))

\[90m\# A tibble: 6 x 2\[39m speed dist \[3m\[90m<dbl>\[39m\[23m
\[3m\[90m<dbl>\[39m\[23m \[90m1\[39m 4 2 \[90m2\[39m 4 10
\[90m3\[39m 7 4 \[90m4\[39m 7 22 \[90m5\[39m 8 16 \[90m6\[39m 9
10

You’ll still need to render `README.Rmd` regularly, to keep `README.md`
up-to-date.

You can also embed plots, for example:

<img src="man/figures/README-pressure-1.png" width="100%" />

In that case, don’t forget to commit and push the resulting figure
files, so they display on GitHub!
