### Conditional Statements
### If statement
**Sample syntax**
```R
if (condition) {
  expr
}
```
You can only use an else statement in combination with an if statement. The else statement does not require a condition:

💡It's important that the else keyword comes on the same line as the closing bracket of the if part!

```R
if (x < 0) {
  print("x is a negative number!")
} else if (x == 0) {
  print("x is zero")
} else {
  print("x is a positive number")
}
```
- Keep in mind that R ignores the remainder of the control structure once a condition has been found that is `TRUE`

**For Loop**
```R
primes <- c(2, 3, 5, 7, 11, 13)

# loop version 1
for (p in primes) {
  print(p)
}

# loop version 2
for (i in 1:length(primes)) {
  print(primes[i])
}
```
**Nested For loop**
```R
for (var1 in seq1) {
  for (var2 in seq2) {
    expr
  }
}
```
- The `break` statement abandons the active loop: the remaining code in the loop is skipped and the loop is not iterated over anymore.
- The `next` statement skips the remainder of the code in the loop, but continues the iteration.
  
