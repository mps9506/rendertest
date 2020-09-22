---
title: "A Book"
author: "Frida Gomam"
site: bookdown::bookdown_site
documentclass: book
output:
  bookdown::gitbook: default
  bookdown::pdf_book: default
---


```r
library(crayon)
library(tibble)
library(fansi)
```


# Hello World

Example with default options.


```r
cat(blue("Hello", "world!\n"))
```

```
## [34mHello world!
## [39m
```

```r
as_tibble(cars)
```

```
## [90m# A tibble: 50 x 2[39m
##    speed  dist
##    [3m[90m<dbl>[39m[23m [3m[90m<dbl>[39m[23m
## [90m 1[39m     4     2
## [90m 2[39m     4    10
## [90m 3[39m     7     4
## [90m 4[39m     7    22
## [90m 5[39m     8    16
## [90m 6[39m     9    10
## [90m 7[39m    10    18
## [90m 8[39m    10    26
## [90m 9[39m    10    34
## [90m10[39m    11    17
## [90m# … with 40 more rows[39m
```

Try fansi hooks


```r
old.hooks <- fansi::set_knit_hooks(knitr::knit_hooks)
```

```
## <STYLE type='text/css' scoped>
## PRE.fansi SPAN {padding-top: .25em; padding-bottom: .25em};
## </STYLE>
```



Please render correctly


```r
cat(blue("Hello", "world!\n"))
```

<PRE class="fansi fansi-output"><CODE>## <span style='color: #0000BB;'>Hello world!
## </span><span>
</span></CODE></PRE>

```r
as_tibble(cars)
```

<PRE class="fansi fansi-output"><CODE>## <span style='color: #555555;'># A tibble: 50 x 2</span><span>
##    speed  dist
##    </span><span style='color: #555555;font-style: italic;'>&lt;dbl&gt;</span><span> </span><span style='color: #555555;font-style: italic;'>&lt;dbl&gt;</span><span>
## </span><span style='color: #555555;'> 1</span><span>     4     2
## </span><span style='color: #555555;'> 2</span><span>     4    10
## </span><span style='color: #555555;'> 3</span><span>     7     4
## </span><span style='color: #555555;'> 4</span><span>     7    22
## </span><span style='color: #555555;'> 5</span><span>     8    16
## </span><span style='color: #555555;'> 6</span><span>     9    10
## </span><span style='color: #555555;'> 7</span><span>    10    18
## </span><span style='color: #555555;'> 8</span><span>    10    26
## </span><span style='color: #555555;'> 9</span><span>    10    34
## </span><span style='color: #555555;'>10</span><span>    11    17
## </span><span style='color: #555555;'># … with 40 more rows</span><span>
</span></CODE></PRE>


Restore default hooks


```r
do.call(knitr::knit_hooks$set, old.hooks)
```


Please render incorrectly


```r
cat(blue("Hello", "world!\n"))
```

```
## [34mHello world!
## [39m
```

```r
as_tibble(cars)
```

```
## [90m# A tibble: 50 x 2[39m
##    speed  dist
##    [3m[90m<dbl>[39m[23m [3m[90m<dbl>[39m[23m
## [90m 1[39m     4     2
## [90m 2[39m     4    10
## [90m 3[39m     7     4
## [90m 4[39m     7    22
## [90m 5[39m     8    16
## [90m 6[39m     9    10
## [90m 7[39m    10    18
## [90m 8[39m    10    26
## [90m 9[39m    10    34
## [90m10[39m    11    17
## [90m# … with 40 more rows[39m
```


<!-- If you need PDF output, uncomment bookdown::pdf_book above in YAML. You will need a LaTeX installation, e.g., https://yihui.name/tinytex/ -->
