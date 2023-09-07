# Functions

Functions are declared using the fn keyword. Its arguments are type annotated, just like variables, and, if the function
returns a value, the return type must be specified after an arrow ->.

The final expression in the function will be used as return value. Alternatively, the return statement can be used to
return a value earlier from within the function, even from inside loops or if statements.

Rust code uses snake case as the conventional style for function and variable names, in which all letters are lowercase
and underscores separate words.

```rust
/// Adds one to the number given.
///
/// # Examples
///
/// ```
/// let arg = 5;
/// let answer = my_crate::add_one(arg);
///
/// assert_eq!(6, answer);
/// ```
pub fn add_one(x: i32) -> i32 {
    x + 1
}

// Example of generic function
pub fn print<T: Debug>(input: T) {
    println!("{:?}", input);
}
```
