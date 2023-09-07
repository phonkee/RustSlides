# Macros

Rust macros are a powerful tool that allow you to write code that writes code. Macros are used to extend the language itself. They are similar to C/C++ macros, but they are much more powerful and safer.
We call them hygienic macros because they are designed to prevent unintended side-effects and bugs.

There are multiple types of macros in Rust:

* Declarative macros with `macro_rules!` syntax
* Procedural macros
  * Custom `#[derive]` macros
  * Attribute-like macros
  * Function-like macros

This solves some of rust limitations. They are powerful and can be used to extend the language itself.
