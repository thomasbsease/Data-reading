Pulling in data
================
Thomas Sease

``` r
library(tidyverse)
```

Let’s first load the data:

``` r
nobel <- read.csv("data-raw/nobel.csv")
```

Then let’s split the data into two:

``` r
# stem laureates
nobel_stem <- nobel %>%
  filter(category %in% c("Physics", "Medicine", "Chemistry", "Economics"))

# non-steam laureates
nobel_non_stem <- nobel %>%
  filter(!(category %in% c("Physics", "Medicine", "Chemistry", "Economics")))
```

And finally write out the data:

``` r
#write_csv(nobel_stem, file = "data/nobel.sem.csv")

#write_csv(nobel_non_stem, "data/non_sem.csv")
```
