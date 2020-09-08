# Closure Error

![](../images/closureError.jpeg)

Often times while indexing, you get the following error:
```r
Error: Object of type 'closure' is not subsettable
```

In short words, this error usually comes when you are trying to index a function and basically states that functions are not subsettable.
``` r
mean[1]
#> Error in mean[1]: object of type 'closure' is not subsettable
```

More on closure: A closure is a record storing a function together with an environment. For example:
``` r
power = function(n){
  function(x) x^n
}

square = power(2)
cube = power(3)

square(5)
#> [1] 25
cube(5)
#> [1] 125

square[1]
#> Error in square[1]: object of type 'closure' is not subsettable
```
