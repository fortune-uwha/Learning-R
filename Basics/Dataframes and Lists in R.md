### Dataframes
The function `str()` shows you the structure of your dataset. For a data frame it tells you:

- The total number of observations 
- The total number of variables 
- A full list of the variables names 
- The data type of each variable (e.g. num)
- The first observations

💡To select a single column you can use the `$` sign:

`planets_df$diameter`

### Subsets:subsetting vectors, dataframe
`subset(my_df, subset = some_condition)` : Return subsets of vectors, matrices or data frames which meet conditions.
**Order**
order() is a function that gives you the ranked position of each element when it is applied on a variable, such as a vector for example:
```R
a <- c(100, 10, 1000)
order(a)
[1] 2 1 3
```

It means we can use order to reshuffle `a`
```R
a[order(a)]
[1]   10  100 1000
```

**Point to note:** What is the difference between `[` and `[[` in R?

* one generally uses `[[` to select any single element, whereas `[` returns a list of the selected elements.
