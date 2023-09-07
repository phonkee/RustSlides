# Ownership and borrowing 2

We can borrow given string so we can use it after function returns back

```rust
// name 
fn print_name(name: &String) {
    println!("Hello, {}!", name);
}

// prepare name variable
let name = "Peter".to_string();

// now we pass ownership to print_name function
print_name(&name);

// This will not compile
println!("{}", name);
```

With mutable borrows we can even modify borrowed variable

```rust
fn update_name(name: &mut String) {
    name.push_str("!");
}

// prepare name variable
let mut name = "Peter".to_string();

// now we pass ownership to print_name function
update_name(&mut name);

// This will not compile
println!("{}", name);

```
