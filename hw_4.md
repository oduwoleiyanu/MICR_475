HW\_4 Notebook
================

``` r
####
## script for Homework4, sum and scatterplot 
#####
library(tidyverse)
library(nycflights13)
a <- 3
b <- 2
# The sum of a and b
print(a+b)
```

    ## [1] 5

``` r
# Using the sum function 
sum(2+3)
```

    ## [1] 5

``` r
#filter AA carrier and convert to data frame
aa_flights <- filter(flights, carrier == "AA")
aa_flights <- as.data.frame(aa_flights)
ggplot(data = aa_flights) +
  geom_point(mapping = aes(x = dep_delay, y = arr_delay)) # relationship between delay and arriver
```

![](hw_4_files/figure-gfm/unnamed-chunk-1-1.png)<!-- -->
