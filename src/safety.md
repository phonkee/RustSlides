# Memory safety


Rust's approach to memory safety is based on two key concepts: ownership and borrowing. 
These concepts are enforced by Rust's compiler and prevent common memory-related bugs like null pointers, use-after-free errors, and buffer overflows.
Ownership is Rust’s most unique feature and has deep implications for the rest of the language. It enables Rust to make memory safety guarantees without needing a garbage collector, so it’s important to understand how ownership works.
