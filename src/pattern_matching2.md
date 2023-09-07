# Pattern matching 2

Every pattern matching must be exhaustive (all possible cases must be covered).
Lets see an enum example:


```rust
enum Color {
    Red,
    Green,
    Blue,
}

let color = Color::Red;

let name = match color {
    Color::Red => "red",
    Color::Green => "green",
};


```
