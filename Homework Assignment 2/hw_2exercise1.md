---
title: "HW02_Assignment1"
output:
    html_document:
      keep_md: true
editor_options: 
  chunk_output_type: inline
---




```r
library(gapminder)
library(tidyverse)
```

Exercise 1.1
Complete exercise and put into new variable

```r
(gapminder_new = gapminder %>% 
  filter(year >= 1970 & year < 1980,
         country == "China" | country == "Croatia" | country == "Haiti"))
```

```
## # A tibble: 6 x 6
##   country continent  year lifeExp       pop gdpPercap
##   <fct>   <fct>     <int>   <dbl>     <int>     <dbl>
## 1 China   Asia       1972    63.1 862030000      677.
## 2 China   Asia       1977    64.0 943455000      741.
## 3 Croatia Europe     1972    69.6   4225310     9164.
## 4 Croatia Europe     1977    70.6   4318673    11305.
## 5 Haiti   Americas   1972    48.0   4698301     1654.
## 6 Haiti   Americas   1977    49.9   4908554     1874.
```

Exercise 1.2 

Select country and gdppercap

```r
gapminder_new %>% 
  select(country, gdpPercap)
```

```
## # A tibble: 6 x 2
##   country gdpPercap
##   <fct>       <dbl>
## 1 China        677.
## 2 China        741.
## 3 Croatia     9164.
## 4 Croatia    11305.
## 5 Haiti       1654.
## 6 Haiti       1874.
```

Exercise 1.3


```r
gapminder %>% 
  arrange(country, lifeExp, year)
```

```
## # A tibble: 1,704 x 6
##    country     continent  year lifeExp      pop gdpPercap
##    <fct>       <fct>     <int>   <dbl>    <int>     <dbl>
##  1 Afghanistan Asia       1952    28.8  8425333      779.
##  2 Afghanistan Asia       1957    30.3  9240934      821.
##  3 Afghanistan Asia       1962    32.0 10267083      853.
##  4 Afghanistan Asia       1967    34.0 11537966      836.
##  5 Afghanistan Asia       1972    36.1 13079460      740.
##  6 Afghanistan Asia       1977    38.4 14880372      786.
##  7 Afghanistan Asia       1982    39.9 12881816      978.
##  8 Afghanistan Asia       1987    40.8 13867957      852.
##  9 Afghanistan Asia       1992    41.7 16317921      649.
## 10 Afghanistan Asia       1997    41.8 22227415      635.
## # … with 1,694 more rows
```

