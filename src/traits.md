# Traits

A trait defines functionality a particular type has and can share with other types. We can use traits to define shared behavior in an abstract way. We can use trait bounds to specify that a generic type can be any type that has certain behavior.

```rust
pub trait Summary {
    fn summarize(&self) -> String;
}
```

There are a lot of traits in the standard library. For example, 
* `ToString` trait is implemented by any type that can be converted into a `String` value. We can use the `to_string` method defined by the `ToString` trait to convert a number into a `String`:
* `Into` trait is implemented by any type that can be converted into another type. 
* `From` trait is implemented by any type that can be created from another type.
* `Debug` trait is used to format a value using the `{:?}` formatter.
* `std::ops` module contains traits for overloading operators.

Some traits can be implemented by deriving them. For example, the `Debug` trait can be implemented by deriving it:

```rust
#[derive(Debug)]
pub struct Point {
    x: i32,
    y: i32,
}
````

This means that they use derive macros to generate the implementation. We can also implement traits manually:

```rust
pub struct Point {
    x: i32,
    y: i32,
}

impl Debug for Point {
    fn fmt(&self, f: &mut Formatter<'_>) -> Result<(), Error> {
        write!(f, "Point {{ x: {}, y: {} }}", self.x, self.y)
    }
}
```

