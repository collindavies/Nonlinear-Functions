Nonlinear Functions
================
Collin Davies
10/5/2021

## P1

Summary: Load the data from the file 7.R.RData, and plot it using
plot(x,y). What is the slope coefficient in a linear regression of y on
x (to within 10%)?

Task 1: Load the data from the file 7.R.RData

``` r
load("7.R.RData")
```

Task 2: Plot the data.

``` r
plot(x,y)
```

![](Nonlinear-Functions_files/figure-gfm/unnamed-chunk-2-1.png)<!-- -->

Task 3: Return slope coefficient in a linear regression of y on x (to
within 10%).

``` r
fita = lm(y~ x)
out <- summary(fita)
out$coefficients[2, 1]
```

    ## [1] -0.6748303

## P2

Summary: For the model y \~ 1+x+x^2, what is the coefficient of x (to
within 10%)?

Task 1: Return slope coefficient of x (to within 10%).

``` r
fitb = lm(y~ 1+x+I(x^2))
out2 <- summary(fitb)
out2$coefficients[2, 1]
```

    ## [1] 77.70751
