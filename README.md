
<!-- README.md is generated from README.Rmd. Please edit that file -->
wtf-packages-report
===================

Overview with first change
--------------------------

The goal of wtf-packages-report is to explore the packages in my R installation.

I have 399 add-on packages installed.

Here's how they break down in terms of which version of R they were built under, which is related to how recently they were updated on CRAN.

| Built |    n|  prop|
|:------|----:|-----:|
| 3.5.0 |  344|  0.86|
| 3.5.1 |   46|  0.12|
| 3.5.2 |    9|  0.02|

![](figs/built-barchart.png)

### Flow of the analysis

Run [R/90\_make-clean.R](R/90_make-clean.R) to clean out downstream products.

Run [R/95\_make-all.R](R/95_make-all.R) to re-run the analysis and re-render this README.

<table>
<colgroup>
<col width="27%" />
<col width="27%" />
<col width="44%" />
</colgroup>
<thead>
<tr class="header">
<th>Input</th>
<th>Script</th>
<th>Output</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><a href="R/01_write-installed-packages.R" class="uri">R/01_write-installed-packages.R</a></td>
<td><a href="data/installed-packages.csv" class="uri">data/installed-packages.csv</a></td>
</tr>
<tr class="even">
<td><a href="data/installed-packages.csv" class="uri">data/installed-packages.csv</a></td>
<td><a href="R/02_wrangle-packages.R" class="uri">R/02_wrangle-packages.R</a></td>
<td><a href="data/add-on-packages.csv" class="uri">data/add-on-packages.csv</a><br><a href="data/add-on-packages-freqtable.csv" class="uri">data/add-on-packages-freqtable.csv</a></td>
</tr>
<tr class="odd">
<td><a href="data/add-on-packages-freqtable.csv" class="uri">data/add-on-packages-freqtable.csv</a></td>
<td><a href="R/03_barchart-packages-built.R" class="uri">R/03_barchart-packages-built.R</a></td>
<td><a href="figs/built-barchart.png" class="uri">figs/built-barchart.png</a></td>
</tr>
</tbody>
</table>

<details>

<summary>Session info</summary>

``` r
devtools::session_info()
#> ─ Session info ──────────────────────────────────────────────────────────
#>  setting  value                       
#>  version  R version 3.4.2 (2017-09-28)
#>  os       macOS  10.14.2              
#>  system   x86_64, darwin15.6.0        
#>  ui       X11                         
#>  language (EN)                        
#>  collate  en_US.UTF-8                 
#>  ctype    en_US.UTF-8                 
#>  tz       America/Chicago             
#>  date     2019-02-04                  
#> 
#> ─ Packages ──────────────────────────────────────────────────────────────
#>  package     * version date       lib source        
#>  assertthat    0.2.0   2017-04-11 [1] CRAN (R 3.4.0)
#>  backports     1.1.1   2017-09-25 [1] CRAN (R 3.4.2)
#>  bindr         0.1     2016-11-13 [1] CRAN (R 3.4.0)
#>  bindrcpp    * 0.2     2017-06-17 [1] CRAN (R 3.4.0)
#>  broom         0.4.3   2017-11-20 [1] CRAN (R 3.4.2)
#>  callr         3.1.1   2018-12-21 [1] CRAN (R 3.4.4)
#>  cellranger    1.1.0   2016-07-27 [1] CRAN (R 3.4.0)
#>  cli           1.0.0   2017-11-05 [1] CRAN (R 3.4.2)
#>  colorspace    1.3-2   2016-12-14 [1] CRAN (R 3.4.0)
#>  crayon        1.3.4   2017-09-16 [1] CRAN (R 3.4.1)
#>  desc          1.2.0   2018-05-01 [1] CRAN (R 3.4.4)
#>  devtools      2.0.1   2018-10-26 [1] CRAN (R 3.4.2)
#>  digest        0.6.12  2017-01-27 [1] CRAN (R 3.4.0)
#>  dplyr       * 0.7.4   2017-09-28 [1] CRAN (R 3.4.2)
#>  evaluate      0.10.1  2017-06-24 [1] CRAN (R 3.4.1)
#>  forcats     * 0.2.0   2017-01-23 [1] CRAN (R 3.4.0)
#>  foreign       0.8-69  2017-06-22 [1] CRAN (R 3.4.2)
#>  fs            1.2.6   2018-08-23 [1] CRAN (R 3.4.4)
#>  ggplot2     * 2.2.1   2016-12-30 [1] CRAN (R 3.4.0)
#>  glue          1.2.0   2017-10-29 [1] CRAN (R 3.4.2)
#>  gtable        0.2.0   2016-02-26 [1] CRAN (R 3.4.0)
#>  haven         1.1.0   2017-07-09 [1] CRAN (R 3.4.1)
#>  here          0.1     2017-05-28 [1] CRAN (R 3.4.0)
#>  highr         0.6     2016-05-09 [1] CRAN (R 3.4.0)
#>  hms           0.4.0   2017-11-23 [1] CRAN (R 3.4.3)
#>  htmltools     0.3.6   2017-04-28 [1] CRAN (R 3.4.0)
#>  httr          1.3.1   2017-08-20 [1] CRAN (R 3.4.1)
#>  jsonlite      1.5     2017-06-01 [1] CRAN (R 3.4.0)
#>  knitr         1.17    2017-08-10 [1] CRAN (R 3.4.1)
#>  lattice       0.20-35 2017-03-25 [1] CRAN (R 3.4.2)
#>  lazyeval      0.2.1   2017-10-29 [1] CRAN (R 3.4.2)
#>  lubridate     1.7.1   2017-11-03 [1] CRAN (R 3.4.2)
#>  magrittr      1.5     2014-11-22 [1] CRAN (R 3.4.0)
#>  memoise       1.1.0   2017-04-21 [1] CRAN (R 3.4.0)
#>  mnormt        1.5-5   2016-10-15 [1] CRAN (R 3.4.0)
#>  modelr        0.1.1   2017-07-24 [1] CRAN (R 3.4.1)
#>  munsell       0.4.3   2016-02-13 [1] CRAN (R 3.4.0)
#>  nlme          3.1-131 2017-02-06 [1] CRAN (R 3.4.2)
#>  pkgbuild      1.0.2   2018-10-16 [1] CRAN (R 3.4.4)
#>  pkgconfig     2.0.1   2017-03-21 [1] CRAN (R 3.4.0)
#>  pkgload       1.0.2   2018-10-29 [1] CRAN (R 3.4.4)
#>  plyr          1.8.4   2016-06-08 [1] CRAN (R 3.4.0)
#>  prettyunits   1.0.2   2015-07-13 [1] CRAN (R 3.4.0)
#>  processx      3.2.1   2018-12-05 [1] CRAN (R 3.4.4)
#>  ps            1.3.0   2018-12-21 [1] CRAN (R 3.4.4)
#>  psych         1.7.8   2017-09-09 [1] CRAN (R 3.4.2)
#>  purrr       * 0.2.4   2017-10-18 [1] CRAN (R 3.4.2)
#>  R6            2.2.2   2017-06-17 [1] CRAN (R 3.4.0)
#>  Rcpp          0.12.14 2017-11-23 [1] CRAN (R 3.4.3)
#>  readr       * 1.1.1   2017-05-16 [1] CRAN (R 3.4.0)
#>  readxl        1.1.0   2018-04-20 [1] CRAN (R 3.4.4)
#>  remotes       2.0.2   2018-10-30 [1] CRAN (R 3.4.4)
#>  reshape2      1.4.2   2016-10-22 [1] CRAN (R 3.4.0)
#>  rlang         0.1.4   2017-11-05 [1] CRAN (R 3.4.2)
#>  rmarkdown     1.8     2017-11-17 [1] CRAN (R 3.4.2)
#>  rprojroot     1.2     2017-01-16 [1] CRAN (R 3.4.0)
#>  rstudioapi    0.7     2017-09-07 [1] CRAN (R 3.4.1)
#>  rvest         0.3.2   2016-06-17 [1] CRAN (R 3.4.0)
#>  scales        0.5.0   2017-08-24 [1] CRAN (R 3.4.1)
#>  sessioninfo   1.1.1   2018-11-05 [1] CRAN (R 3.4.4)
#>  stringi       1.1.6   2017-11-17 [1] CRAN (R 3.4.2)
#>  stringr     * 1.2.0   2017-02-18 [1] CRAN (R 3.4.0)
#>  tibble      * 1.3.4   2017-08-22 [1] CRAN (R 3.4.1)
#>  tidyr       * 0.7.2   2017-10-16 [1] CRAN (R 3.4.2)
#>  tidyverse   * 1.2.1   2017-11-14 [1] CRAN (R 3.4.2)
#>  usethis       1.4.0   2018-08-14 [1] CRAN (R 3.4.4)
#>  withr         2.1.2   2018-03-15 [1] CRAN (R 3.4.4)
#>  xml2          1.1.1   2017-01-24 [1] CRAN (R 3.4.0)
#>  yaml          2.1.15  2017-12-01 [1] CRAN (R 3.4.3)
#> 
#> [1] /Library/Frameworks/R.framework/Versions/3.4/Resources/library
```

</details>
