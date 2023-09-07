# Modules

Rust provides a powerful module system that can be used to hierarchically split code in logical units (modules), and manage visibility (public/private) between them.

A module is a collection of items: functions, structs, traits, impl blocks, and even other modules.

```shell
.
├── Cargo.toml
└── src
    └── lib.rs
    └── module
      └── mod.rs
      └── hello.rs
```

In mod.rs we need to add `pub mod hello;` to make it visible to the outside world.

```rust
pub mod hello;
```

Also in lib.rs we need to have

```rust
pub mod module;
```

You can also provide modules directly in rust file

```rust
pub mod hello {
    pub fn world() {
        println!("Hello, world!");
    }
}
```