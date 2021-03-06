
<!-- README.md is generated from README.Rmd. Please edit that file -->

``` r
knitr::opts_chunk$set(
  collapse = TRUE,
  comment = "#>",
  fig.path = "man/figures/README-",
  out.width = "100%"
)

library(tibble)
library(crayon)

## from: https://github.com/r-lib/crayon/issues/96
# options(crayon.enabled = NULL)
```

# rendertest

Trying to figure out encoding problems when I use github actions to
render readme and pkgdown websites.

``` r
.Platform
#> $OS.type
#> [1] "unix"
#> 
#> $file.sep
#> [1] "/"
#> 
#> $dynlib.ext
#> [1] ".so"
#> 
#> $GUI
#> [1] "X11"
#> 
#> $endian
#> [1] "little"
#> 
#> $pkgType
#> [1] "source"
#> 
#> $path.sep
#> [1] ":"
#> 
#> $r_arch
#> [1] ""
```

``` r
crayon::has_color()
#> [1] FALSE
```

``` r
er <- errorCondition(
  message = paste("crayon::has_color() ?:",
                  crayon::has_color(),
                  "\nresult:",
                  crayon::red("A barfoo error")))
er
#> <error: crayon::has_color() ?: FALSE 
#> result: A barfoo error>
```

## Example

Print a tibble:

``` r
as_tibble(cars)
#> # A tibble: 50 x 2
#>    speed  dist
#>    <dbl> <dbl>
#>  1     4     2
#>  2     4    10
#>  3     7     4
#>  4     7    22
#>  5     8    16
#>  6     9    10
#>  7    10    18
#>  8    10    26
#>  9    10    34
#> 10    11    17
#> # … with 40 more rows
```

## unicode

Print some unicode: Plain old unicode seems to work.

Ā ā Ġ ☂

## Example Crayon

print using crayon directly

``` r
cat(blue("Hello", "world!\n"))
#> Hello world!
```

## Set options in yaml

``` yml
    - uses: r-lib/actions/setup-r@v1
      with:
        crayon.enabled: FALSE
```

reset option

``` r

options(crayon.enabled = TRUE)

cat(blue("Hello", "world!\n"))
#> [34mHello world!
#> [39m

as_tibble(cars)
#> [90m# A tibble: 50 x 2[39m
#>    speed  dist
#>    [3m[90m<dbl>[39m[23m [3m[90m<dbl>[39m[23m
#> [90m 1[39m     4     2
#> [90m 2[39m     4    10
#> [90m 3[39m     7     4
#> [90m 4[39m     7    22
#> [90m 5[39m     8    16
#> [90m 6[39m     9    10
#> [90m 7[39m    10    18
#> [90m 8[39m    10    26
#> [90m 9[39m    10    34
#> [90m10[39m    11    17
#> [90m# … with 40 more rows[39m
```

Try `fansi`

``` r
old.hooks <- fansi::set_knit_hooks(knitr::knit_hooks)
#> <STYLE type='text/css' scoped>
#> PRE.fansi SPAN {padding-top: .25em; padding-bottom: .25em};
#> </STYLE>
```

check output

``` r

cat(blue("Hello", "world!\n"))
```

<PRE class="fansi fansi-output"><CODE>#&gt; <span style='color: #0000BB;'>Hello world!
#&gt; </span><span>
</span></CODE></PRE>

``` r

as_tibble(cars)
```

<PRE class="fansi fansi-output"><CODE>#&gt; <span style='color: #555555;'># A tibble: 50 x 2</span><span>
#&gt;    speed  dist
#&gt;    </span><span style='color: #555555;font-style: italic;'>&lt;dbl&gt;</span><span> </span><span style='color: #555555;font-style: italic;'>&lt;dbl&gt;</span><span>
#&gt; </span><span style='color: #555555;'> 1</span><span>     4     2
#&gt; </span><span style='color: #555555;'> 2</span><span>     4    10
#&gt; </span><span style='color: #555555;'> 3</span><span>     7     4
#&gt; </span><span style='color: #555555;'> 4</span><span>     7    22
#&gt; </span><span style='color: #555555;'> 5</span><span>     8    16
#&gt; </span><span style='color: #555555;'> 6</span><span>     9    10
#&gt; </span><span style='color: #555555;'> 7</span><span>    10    18
#&gt; </span><span style='color: #555555;'> 8</span><span>    10    26
#&gt; </span><span style='color: #555555;'> 9</span><span>    10    34
#&gt; </span><span style='color: #555555;'>10</span><span>    11    17
#&gt; </span><span style='color: #555555;'># … with 40 more rows</span><span>
</span></CODE></PRE>

``` r

er
#> <error: crayon::has_color() ?: FALSE 
#> result: A barfoo error>
```

## session

``` r
sessioninfo::session_info()
#> ─ Session info ───────────────────────────────────────────────────────────────
#>  setting  value                       
#>  version  R version 4.0.2 (2020-06-22)
#>  os       Ubuntu 18.04.5 LTS          
#>  system   x86_64, linux-gnu           
#>  ui       X11                         
#>  language (EN)                        
#>  collate  C.UTF-8                     
#>  ctype    C.UTF-8                     
#>  tz       UTC                         
#>  date     2020-09-24                  
#> 
#> ─ Packages ───────────────────────────────────────────────────────────────────
#>  package     * version date       lib source        
#>  assertthat    0.2.1   2019-03-21 [1] CRAN (R 4.0.2)
#>  cli           2.0.2   2020-02-28 [1] CRAN (R 4.0.2)
#>  crayon      * 1.3.4   2017-09-16 [1] CRAN (R 4.0.2)
#>  digest        0.6.25  2020-02-23 [1] CRAN (R 4.0.2)
#>  ellipsis      0.3.1   2020-05-15 [1] CRAN (R 4.0.2)
#>  evaluate      0.14    2019-05-28 [1] CRAN (R 4.0.2)
#>  fansi         0.4.1   2020-01-08 [1] CRAN (R 4.0.2)
#>  glue          1.4.2   2020-08-27 [1] CRAN (R 4.0.2)
#>  htmltools     0.5.0   2020-06-16 [1] CRAN (R 4.0.2)
#>  knitr         1.30    2020-09-22 [1] CRAN (R 4.0.2)
#>  lifecycle     0.2.0   2020-03-06 [1] CRAN (R 4.0.2)
#>  magrittr      1.5     2014-11-22 [1] CRAN (R 4.0.2)
#>  pillar        1.4.6   2020-07-10 [1] CRAN (R 4.0.2)
#>  pkgconfig     2.0.3   2019-09-22 [1] CRAN (R 4.0.2)
#>  rlang         0.4.7   2020-07-09 [1] CRAN (R 4.0.2)
#>  rmarkdown     2.3     2020-06-18 [1] CRAN (R 4.0.2)
#>  sessioninfo   1.1.1   2018-11-05 [1] CRAN (R 4.0.2)
#>  stringi       1.5.3   2020-09-09 [1] CRAN (R 4.0.2)
#>  stringr       1.4.0   2019-02-10 [1] CRAN (R 4.0.2)
#>  tibble      * 3.0.3   2020-07-10 [1] CRAN (R 4.0.2)
#>  utf8          1.1.4   2018-05-24 [1] CRAN (R 4.0.2)
#>  vctrs         0.3.4   2020-08-29 [1] CRAN (R 4.0.2)
#>  withr         2.3.0   2020-09-22 [1] CRAN (R 4.0.2)
#>  xfun          0.17    2020-09-09 [1] CRAN (R 4.0.2)
#>  yaml          2.2.1   2020-02-01 [1] CRAN (R 4.0.2)
#> 
#> [1] /home/runner/work/_temp/Library
#> [2] /opt/R/4.0.2/lib/R/library
```
