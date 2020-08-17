
<!-- README.md is generated from README.Rmd. Please edit that file -->

# rendertest

Trying to figure out encoding problems when I use github actions to
render readme and pkgdown websites.

## Example

What is special about using `README.Rmd` instead of just `README.md`?
You can include R chunks like so:

``` r
head(tibble::as_tibble(cars))
#> [90m# A tibble: 6 x 2[39m
#>   speed  dist
#>   [3m[90m<dbl>[39m[23m [3m[90m<dbl>[39m[23m
#> [90m1[39m     4     2
#> [90m2[39m     4    10
#> [90m3[39m     7     4
#> [90m4[39m     7    22
#> [90m5[39m     8    16
#> [90m6[39m     9    10
```

You’ll still need to render `README.Rmd` regularly, to keep `README.md`
up-to-date.

You can also embed plots, for example:

<img src="man/figures/README-pressure-1.png" width="100%" />

In that case, don’t forget to commit and push the resulting figure
files, so they display on GitHub\!

``` r
sessioninfo::session_info()
#> ─ Session info ───────────────────────────────────────────────────────────────
#>  setting  value                       
#>  version  R version 4.0.2 (2020-06-22)
#>  os       Ubuntu 18.04.4 LTS          
#>  system   x86_64, linux-gnu           
#>  ui       X11                         
#>  language (EN)                        
#>  collate  C.UTF-8                     
#>  ctype    C.UTF-8                     
#>  tz       UTC                         
#>  date     2020-08-17                  
#> 
#> ─ Packages ───────────────────────────────────────────────────────────────────
#>  package     * version date       lib source        
#>  assertthat    0.2.1   2019-03-21 [1] CRAN (R 4.0.2)
#>  cli           2.0.2   2020-02-28 [1] CRAN (R 4.0.2)
#>  crayon        1.3.4   2017-09-16 [1] CRAN (R 4.0.2)
#>  digest        0.6.25  2020-02-23 [1] CRAN (R 4.0.2)
#>  ellipsis      0.3.1   2020-05-15 [1] CRAN (R 4.0.2)
#>  evaluate      0.14    2019-05-28 [1] CRAN (R 4.0.2)
#>  fansi         0.4.1   2020-01-08 [1] CRAN (R 4.0.2)
#>  glue          1.4.1   2020-05-13 [1] CRAN (R 4.0.2)
#>  htmltools     0.5.0   2020-06-16 [1] CRAN (R 4.0.2)
#>  knitr         1.29    2020-06-23 [1] CRAN (R 4.0.2)
#>  lifecycle     0.2.0   2020-03-06 [1] CRAN (R 4.0.2)
#>  magrittr      1.5     2014-11-22 [1] CRAN (R 4.0.2)
#>  pillar        1.4.6   2020-07-10 [1] CRAN (R 4.0.2)
#>  pkgconfig     2.0.3   2019-09-22 [1] CRAN (R 4.0.2)
#>  rlang         0.4.7   2020-07-09 [1] CRAN (R 4.0.2)
#>  rmarkdown     2.3     2020-06-18 [1] CRAN (R 4.0.2)
#>  sessioninfo   1.1.1   2018-11-05 [1] CRAN (R 4.0.2)
#>  stringi       1.4.6   2020-02-17 [1] CRAN (R 4.0.2)
#>  stringr       1.4.0   2019-02-10 [1] CRAN (R 4.0.2)
#>  tibble        3.0.3   2020-07-10 [1] CRAN (R 4.0.2)
#>  utf8          1.1.4   2018-05-24 [1] CRAN (R 4.0.2)
#>  vctrs         0.3.2   2020-07-15 [1] CRAN (R 4.0.2)
#>  withr         2.2.0   2020-04-20 [1] CRAN (R 4.0.2)
#>  xfun          0.16    2020-07-24 [1] CRAN (R 4.0.2)
#>  yaml          2.2.1   2020-02-01 [1] CRAN (R 4.0.2)
#> 
#> [1] /home/runner/work/_temp/Library
#> [2] /opt/R/4.0.2/lib/R/library
```
