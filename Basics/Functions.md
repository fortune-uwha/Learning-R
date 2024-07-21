### Functions in R
To consult the documentation on the `sample()` function for instance;

```R
help(sample)
?sample
```
This way you can clarify what argument a function expects 
- A quick hack to see just the arguments of the `sample()` function is the `args()` function.
```R
args(sample)
```
### Writing your functions
**Function template:**
```R
my_fun <- function(arg1, arg2) {
  body
}
```
* This creates a new R variable `my_fun`, that becomes available in the workspace as soon as you execute it. From then on, you can use the `my_fun` as a function.

**Example**
```R
throw_die <- function() {
  number <- sample(1:6, size = 1)
  number
}

throw_die()
```

