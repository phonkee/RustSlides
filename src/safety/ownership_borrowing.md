# Ownership and borrowing

Ownership is Rust’s most unique feature and has deep implications for the rest of the language. It enables Rust to make memory safety guarantees without needing a garbage collector, so it’s important to understand how ownership works.

```rust
// name argument is now owned by print_name function
fn print_name(name: String) {
    println!("Hello, {}!", name);
}

// prepare name variable
let name = "Peter".to_string();

// now we pass ownership to print_name function
print_name(name);

// This will not compile
println!("{}", name);
```