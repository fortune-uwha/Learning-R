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
if (condition) {
  expr1
} else {
  expr2
}
```
- Keep in mind that R ignores the remainder of the control structure once a condition has been found that is `TRUE`

