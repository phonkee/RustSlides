# Lifetimes

A lifetime is a construct of the compiler (or more specifically, its borrow checker) uses to ensure all borrows are
valid. Specifically, a variable's lifetime begins when it is created and ends when it is destroyed. While lifetimes and
scopes are often referred to together, they are not the same.

Take, for example, the case where we borrow a variable via &. The borrow has a lifetime that is determined by where it
is declared. As a result, the borrow is valid as long as it ends before the lender is destroyed. However, the scope of
the borrow is determined by where the reference is used.

```rust
fn longest<'a>(
    x: &'a str,
    y: &'a str,
) -> &'a str {
    if x.len() > y.len() {
        x
    } else {
        y
    }
}
```