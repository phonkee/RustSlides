# Basic types

Rust provides basic types similar to other programming languages:

- signed integers: `i8`, `i16`, `i32`, `i64`, `i128`, `isize`
- unsigned integers: `u8`, `u16`, `u32`, `u64`, `u128`, `usize`
- floating point: `f32`, `f64`
- boolean: `bool`
- strings: `&str` and `String` (we have way to many string types)
- structs: `struct`
- tuples: `tuple`
- enums: `enum`
- arrays: `[T; N]`
- unit type: `()`

Type inference is a feature of Rust that allows the compiler to determine the type of a value based on the context in
which it is used. This means that, in many cases, you don't need to explicitly specify the type of a variable or
function parameter.

```rust
fn main() {
    // Because of the annotation, the compiler knows that `elem` has type u8.
    let elem = 5u8;

    // Create an empty vector (a growable array).
    let mut vec = Vec::new();
    // At this point the compiler doesn't know the exact type of `vec`, it
    // just knows that it's a vector of something (`Vec<_>`).

    // Insert `elem` in the vector.
    vec.push(elem);
    // Aha! Now the compiler knows that `vec` is a vector of `u8`s (`Vec<u8>`)
    // TODO ^ Try commenting out the `vec.push(elem)` line

    println!("{:?}", vec);
}
```
