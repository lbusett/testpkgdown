
<!-- README.md is generated from README.Rmd. Please edit that file -->

# test

test Rmd to highlight issue 1278
(<https://github.com/r-lib/pkgdown/issues/1278>)

## Example

Using “=” to assign, the chunk is rendered properly:

``` r
# random comment
# 
a = 4
# random comment
cars2 = cars %>% 
    dplyr::filter(speed > 12)

cars2 = dplyr::filter(cars,
                      speed > 12)

#Additional content
cars
```

Using “\<-” to assign, something strange happens.

In the first case, the “= cars %\>” part goes missing.

``` r
# random comment
# 
a = 4
# random comment
cars2 <- cars %>% 
    dplyr::filter(speed > 12)

#Additional content
cars
```

In the second case, we miss also a part of the second line
(“dplyr::filter(cars, speed \>”)

``` r
# random comment
# 
a = 4
# random comment
cars2 <- dplyr::filter(cars,
                       speed > 12)

#Additional content
cars
```
