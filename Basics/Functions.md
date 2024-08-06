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

Sample function that does not require an input.

```R
throw_die <- function() {
  number <- sample(1:6, size = 1)
  number
}
throw_die()
```
**Function scoping**

It implies that variables that are defined inside a function are not accessible outside that function.

**Lapply, sapply, vapply**

The first argument of `sapply()` is the list or vector X over which you want to apply a function, `FUN`.

```R
sapply(X, FUN, ...)
```
Potential additional arguments to this function are specified afterwards (...)

**Difference between lapply and sapply?**

The `lapply` returns a list, while the `sapply` returns a vector that is a simplified version of this list.
