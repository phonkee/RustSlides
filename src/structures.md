# Structures

There are three types of structures ("structs") that can be created using the struct keyword:

* Tuple structs, which are, basically, named tuples.
* The classic C structs
* Unit structs, which are field-less, are useful for generics.

```rust
#[derive(Debug, Default)]
#[repr(C)]
struct Person {
    name: String,
    age: u8,
}

// A unit struct
struct Unit;

// A tuple struct
struct Pair(i32, f32);
```

Implementations of structs

```rust
impl Person {
    fn new(name: String) -> Val {
        Person {
            name,
            ..Default::default()
        }
    }
    fn set_name(&mut self, name: String) -> &f64 {
        &self.name = name;
    }
    fn print_name(&self) {
        println!("Name: {}", self.name);
    }
    fn into_string(self) -> String {
        format!("Hello {}, age: {}", self.name, self.age)
    }
}
```
