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
* R knows what to do when you pass a logical vector in square brackets: it will only select the elements that correspond to `TRUE`

### Matrix
**What is a Matrix?**
```R
matrix(1:9, byrow = TRUE, nrow = 3)
```
In the `matrix()` function:

* The first argument is the collection of elements that R will arrange into the rows and columns of the matrix. Here, we use `1:9` which is a shortcut for `c(1, 2, 3, 4, 5, 6, 7, 8, 9)`.
* The argument `byrow` indicates that the matrix is filled by the rows. If we want the matrix to be filled by the columns, we just place `byrow = FALSE`.
* The third argument `nrow` indicates that the matrix should have three rows.

**Naming a Matrix**

Similar to vectors, you can add names for the rows and the columns of a matrix
```R
rownames(my_matrix) <- row_names_vector
colnames(my_matrix) <- col_names_vector
```
💡In R, the function `rowSums()` conveniently calculates the totals for each row of a matrix. This function creates a new vector:

```R
rowSums(my_matrix)
```
**Sample matrix**
```R
# Construct star_wars_matrix
box_office <- c(460.998, 314.4, 290.475, 247.900, 309.306, 165.8)
region <- c("US", "non-US")
titles <- c("A New Hope", 
                 "The Empire Strikes Back", 
                 "Return of the Jedi")
               
star_wars_matrix <- matrix(box_office, 
                      nrow = 3, byrow = TRUE,
                      dimnames = list(titles, region))
```
**Adding a column to a matrix**
You can add a column or multiple columns to a matrix with the `cbind()` function, which merges matrices and/or vectors together by column. For example:

```R
big_matrix <- cbind(matrix1, matrix2, vector1 ...)
```
