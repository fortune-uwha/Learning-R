## Introduction to R
### Arithmetic with R
In its most basic form, R can be used as a simple calculator. Consider the following arithmetic operators:

* Addition: +
* Subtraction: -
* Multiplication: *
* Division: /
* Exponentiation: ^
* Modulo: %%
  
The last two might need some explaining:

- The ^ operator raises the number to its left to the power of the number to its right: for example 3^2 is 9.
- The modulo returns the remainder of the division of the number to the left by the number on its right, for example 5 modulo 3 or 5 %% 3 is 2.
### What's that data type?
You can check the data type of a variable beforehand. You can do this with the `class()` function
### Vectors
Vectors are one-dimension arrays that can hold numeric data, character data, or logical data. In other words, a vector is a simple tool to store data.
In R, you create a vector with the combine function `c()`. You place the vector elements separated by a comma between the parentheses.
* You can give a name to the elements of a vector with the `names()` function. Example
  ```R
  some_vector <- c("John Doe", "poker player")
  names(some_vector) <- c("Name", "Profession")
```
# Output
Name     Profession 
    "John Doe" "poker player"
```


* `sum()`: It calculates the sum of all elements of a vector.
* the first element in a vector has `index 1`, not 0 as in many other programming languages
* suppose you want to select the first and the fifth day of the week: use the vector c(1, 5) between the square brackets. For example, the code below selects the first and fifth element of poker_vector:

```r
poker_vector[c(1, 5)]
```
