# Iterators and Cosures

Rust’s design has taken inspiration from many existing languages and techniques, and one significant influence is
functional programming. Programming in a functional style often includes using functions as values by passing them in
arguments, returning them from other functions, assigning them to variables for later execution, and so forth.

```rust
let v1 = vec![1, 2, 3];

let v1_iter = v1.iter();

for val in v1_iter {
println!("Got: {}", val);
}
```

Or even more complicated use of iterator

```rust
let x = (1..10)
    .map(|x| x + 1)
    .filter(|x| x % 2 == 0)
    .map(|x| x.to_string())
    .collect::<Vec<_>>();
```

