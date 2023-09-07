# `Option<T>`

Option type is a type that represents an optional value. It is either `Some(value)` or `None`.

```rust
pub type Option<T> {
    pub Some(T),
    pub None
}
```

Pattern matching is a way to extract data from an Option.

```rust
let x = Some(5);

match x {
    Some(i) => println!("i = {}", i),
    None => println!("no value"),
}
```
