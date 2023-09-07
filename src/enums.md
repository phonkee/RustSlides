# Enums

An enum in Rust is a type that represents data that is one of several possible variants. Each variant in the enum can
optionally have data associated with it:

```rust
enum Message {
    Quit,
    ChangeColor(i32, i32, i32),
    Move { x: i32, y: i32 },
    Write(String),
}
```
