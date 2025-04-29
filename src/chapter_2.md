# Functions
- Made of statements and optionally ending in an expression
- Function and variable names are conventionally lowercase with underscores as word separators
- The function `main` is often the entry point of a program and is expected without explicit opt-out
- A function is defined such as `fn main() {  }`
- A function is called by entering its name followed by a set of parentheses
- Functions can be declared and called out of order

### Parameters
- Special variables that are part of a function's signature
- A value assigned to a parameter is called an argument
- The parameter type must be specified
- `fn function(x: i32) {  }`
- Separate multiple parameters with commas

### Statements
- Statements are instructions that perform actions but do not return a value
- Function definitions are statements
- `let y = 6;`

### Expressions
- Expressions are instructions that evaluate to a resulting value
- Expressions can be part of statements
- Calling a function or macro is an expression
- `6`, `5+6`, `{ let x = 3; x + 1 }`

### Functions with Return Values
