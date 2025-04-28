# Data Types
### Variables
- By default variables are immutable, but can be made mutable using the `mut` keyword
- Variables can be declared using the `let` keyword and assigned a value using the `=` operator
- When a new variable is declared with the same name as a previous variable, the first variable is shadowed.
- The second variable overshadows the first until either it itself is shadowed or the scope ends.
- Shadowing can be used to change the type of value while reusing the same name.

### Constants
- Constants are always immutable and the type of value must be annotated
- Constants cant be declared using the `const` keyword and assigned a value using the `=` operator
- Constant naming convention is all uppercase with underscores between words

### Integers
- An integer is a number without a fractional component
- Signed integers are able to be negative and must include a sign. Unsigned integers are always positive.
- `arch` integers are platform-dependent integer types that represent the native word size of the target architecture

| Length  | Signed | Unsigned |
|---------|--------|----------|
| 8-bit   | i8     | u8       |
| 16-bit  | i16    | u16      |
| 32-bit  | i32    | u32      |
| 64-bit  | i64    | u64      |
| 128-bit | i128   | u128     |
| arch    | isize  | usize    |

- Integer literals can be written in any of the forms in the following table
- Number literals that can be multiple types allow a type suffix, such as `57u8`
- Number literals can also use `_` as a visual separator

| Number literals | Example |
|-----------------|---------|
| Decimal         | 98_22   |
| Hex             | 0xff    |
| Octal           | 0o77    |
| Binary          | 0b1111_0000|
| Byte (u8 only)  | b'A'    |

- Integer overflow occurs when the value exceeds the maximum or minimum value that can be represented by the integer type
- If compiling in release mode, integer overflow will wrap around to the minimum value a type can hold
- To explicitly handle overflow, use the following methods provided bt the standard library

| Method        | Handling                           |
|---------------|------------------------------------|
| wrapping_*    | wrap in all modes                  |
| checked_*     | return `none` value                |
| overflowing_* | return value and boolean           |
| saturating_*  | saturate at the values min or max |

### Floating Point Numbers
- Floating point numbers are numbers with a fractional component
- All floating point types are signed
- Floating point numbers are represented using the `f32` and `f64` types
- The default type is `f64`
### Numeric Operations
- Integer division truncates toward zero to the nearest integer (rounds down)

| Operations      | `let` statement usage          | Result |
|-----------------|--------------------------------|--------|
| Addition        | `let sum = 5 + 10;`            | 15     |
| Subtraction     | `let difference = 95.5 - 4.3;` | 91.2   |
| Multiplication  | `let product = 4 * 30;`        | 120    |
| Division (float)| `let quotient = 56.7 / 32.2;`  | 1.7609 |
| Division (int)  | `let truncated = -5 / 3;`      | -1     |
| Remainder       | `let remainder = 43 % 5;`      | 3      |

### Booleans
- A boolean has two possible values: `true` and `false`
- A boolean is one byte in size and is specified using `bool`
- Main usage is through conditionals, such as an if expression
-  `let t = true;` or `let f: bool = false;`

### Characters
- A character type is four bytes in size and is specified with single quotes
- Represents a Unicode Scalar Value
- `let c = 'z';` or `let z: char = 'Z';`

### Tuples
- A tuple is a way to group multiple values with verying types into one compound type
- Once declared, a tuple has a fixed length and cannot grow or shrink
- `let tup: (i32, f64, u8) = (500, 6.4, 1);`
- `let tup = (500, 6.4, 1); let (x, y, z) = tup;`
- `let x = tup.0; let y = tup.1; let z = tup.2`

### Arrays
- An array groups mutiple values of the same type
- Once declared, an array has a fixed length
- `let a = [1, 2, 3, 4, 5];`
- `let first = a[0]; let second = a[1];`
