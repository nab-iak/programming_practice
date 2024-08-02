
# OutLine

- [OutLine](#outline)
- [Practice for R language with difficulty 8 kyu](#practice-for-r-language-with-difficulty-8-kyu)
- [1. Even or Odd](#1-even-or-odd)
# Practice for R language with difficulty 8 kyu
All the questions are from [Codewars](https://www.codewars.com).

# 1. Even or Odd
Create a function that takes an integer as an argument and returns `"Even"` for even numbers or `"Odd"` for odd numbers.

**Solution:**
```r
even_or_odd <- function(n) {
  if ((n %% 2)==0){
    return("Even")
  } else{
    return("Odd")
  }
}
```

**The better solutions:**
```r
# by @liuhui998, @accord75, ...
even_or_odd <- function(n) {
  # your code here
  ifelse((n %% 2) == 0,"Even","Odd")
}
```

```r
# by @RazNaot, @sj95126
even_or_odd <- function(n) {
  c('Even','Odd')[n%%2+1]
}
```

