# Immutability by default

Rust variables are immutable by default

```rust
let hello = 42;
hello = 43;
```

We need to explicitly mark variable as mutable by using `mut` keyword

```rust
fn main() {
    let mut sum = 0;
    for i in 0..5 {
        sum += i;
    }
    println!("sum is {}", sum);
}
```

