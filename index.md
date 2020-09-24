---
title: "A Book"
author: "Frida Gomam"
site: bookdown::bookdown_site
documentclass: book
output:
  bookdown::gitbook: default
  bookdown::pdf_book:
    latex_engine: lualatex
---


```r
library(crayon)
library(tibble)
```


# Hello World

Example with default options.


```r
as_tibble(cars)
```

```
## # A tibble: 50 x 2
##    speed  dist
##    <dbl> <dbl>
##  1     4     2
##  2     4    10
##  3     7     4
##  4     7    22
##  5     8    16
##  6     9    10
##  7    10    18
##  8    10    26
##  9    10    34
## 10    11    17
## # ... with 40 more rows
```




<!-- If you need PDF output, uncomment bookdown::pdf_book above in YAML. You will need a LaTeX installation, e.g., https://yihui.name/tinytex/ -->
