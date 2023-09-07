# `Result<T, E>`

Result type represent either success (`Ok`) or failure (`Err`).
It provides a lot of useful methods to inspect it. We can use pattern matching to extract data from a `Result`.

```rust
let result: Result<i32, ()> = Ok(5);

match result {
    Ok(i) => println!("i = {}", i),
    Err(_) => println!("no value"),
}
```
