# Error handling

Matching on result (and option) is nice, but it would be tedious to write this code every time we want to extract data from a `Result`.
That's where `?` operator comes in handy.

```rust,editable
pub fn process() -> Result<String, String> {
    Ok("ok".to_string())
}

pub fn outer() -> Result<String, String> {
    let result = process()?;
    Ok(result)
}
```

`?` operator can be used only in functions that return `Result` or `Option`.


