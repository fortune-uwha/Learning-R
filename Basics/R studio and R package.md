### Overview
* R studio is an environment that has been created to make your work in R more pleasurable and aesthetically more pleasing so that you can save things that are more efficient than just working in R itself.
* Think of R studio as a shell on top of R and all it does is it takes all of this code that you create and it copies it into the console and then it runs it 

### Load an R Package
There are basically two extremely important functions when it comes down to R packages:

- `install.packages()`, which as you can expect, installs a given package.
- `library()` which loads packages, i.e. attaches them to the `search` list on your R workspace.

**Note:**
  -`search()`, is used to look at the currently attached packages

**Both `library` and `require` are used to load packages so whats the difference?**

- `require` is used inside functions, as it outputs a warning and continues if the package is not found, whereas `library` will throw an error. 
- `require` breaks one of the fundamental rules of robust software systems: _fail early_. your code might yield different, erroneous results, without signalling an error. This is rare but not hypothetical! 
- In most other cases it is better to use `library()`, because this will give an error message at package loading time if the package is not available. `require()` will just fail without an error if the package is not there.
  

