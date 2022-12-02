README
================
2022-12-01

A total of 3 datasets will be used in this project. The first two are
from US Center for Disease Control and Prevention, and the third one are
from United States Census Bureau (an official website of the United
State Government).

1.  The fisrt dataset is “Vaccine Hesitancy for COVID-19: County and
    local estimates” from
    <https://data.cdc.gov/Vaccinations/Vaccine-Hesitancy-for-COVID-19-County-and-local-es/q9mh-h2tw>
    It can be aquired through webscraping by executing the code below.

``` r
library(RSocrata)

read.socrata(
  "https://data.cdc.gov/resource/q9mh-h2tw.json",
  app_token = "trg1fGPbmeJk0ZrQSlXmQMTBV",
  email     = "tzuyuhua@usc.edu",
  password  = "CodingCary0130"
)
```

2.  The second dataset is “United States COVID-19 Cases and Deaths by
    State over Time” from
    <https://data.cdc.gov/Case-Surveillance/United-States-COVID-19-Cases-and-Deaths-by-State-o/9mfq-cb36>
    It can be aquired through webscraping by executing the code below.

``` r
read.socrata(
  "https://data.cdc.gov/resource/9mfq-cb36.json",
  app_token = "Sc1lehIxeCtFlCTmvmYgobCJD",
  email     = "tzuyuhua@usc.edu",
  password  = "CodingCary0130"
)
```

3.  And for the comparison between states summary statistics to be
    reasonable and effective, I need the population data of different
    places. “County Population Totals: 2020-2021” from
    <https://www.census.gov/data/tables/time-series/demo/popest/2020s-counties-total.html>
    A copy of this file is also located in this folder.

``` r
read_excel("data/co-est2021-pop.xlsx", range = "A6:D3149", col_names = FALSE)
```
