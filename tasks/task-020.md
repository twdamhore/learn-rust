# Lesson 020: Methods and associated functions (impl blocks)

## Section 5: Structuring Data

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Write `impl` blocks to define methods on structs, understanding that methods take `&self`, `&mut self`, or `self` as the first parameter
- [ ] Define associated functions (no `self` parameter) such as constructors like `Rectangle::new(width: f64, height: f64) -> Rectangle`, and call them with `::` syntax
- [ ] Understand that Rust has automatic referencing and dereferencing for method calls -- calling `obj.method()` automatically adds `&`, `&mut`, or `*` as needed
- [ ] Use multiple `impl` blocks for the same struct and understand when this is useful (e.g., separating generic impl blocks, conditional trait implementations)
- [ ] Compare Rust methods with Java instance methods and Go receiver functions, noting that Rust methods choose ownership semantics explicitly

## Exercises
- [ ] **Exercise 1 - Rectangle methods**: Add an `impl` block to the `Rectangle` struct from lesson 019 with methods: `area(&self) -> f64`, `perimeter(&self) -> f64`, and `can_hold(&self, other: &Rectangle) -> bool` (returns true if `self` can fully contain `other`). Write tests for each method.
- [ ] **Exercise 2 - Constructor pattern**: Add an associated function `Rectangle::new(width: f64, height: f64) -> Rectangle` and a `Rectangle::square(size: f64) -> Rectangle` constructor. Compare this pattern with Java's `new Rectangle(...)` and Go's `NewRectangle(...)` convention.
- [ ] **Exercise 3 - Builder-style methods**: Create a `Config` struct with fields `host: String`, `port: u16`, `max_connections: u32`, `verbose: bool`. Write a `Config::new()` constructor that provides starting values. (The `Default` trait is covered in lesson 044.) Implement builder-style methods that take `self` (by value) and return `Self`: `with_host(self, host: String) -> Self`, `with_port(self, port: u16) -> Self`, etc. Use method chaining: `Config::new().with_host(String::from("localhost")).with_port(8080)`.
- [ ] **Exercise 4 - Mutable methods**: Create a `Counter` struct with a `count: i64` field. Implement `increment(&mut self)`, `decrement(&mut self)`, `reset(&mut self)`, and `value(&self) -> i64`. Demonstrate the difference between `&self` and `&mut self` by trying to call `increment` on a non-mut binding.

## Notes
_Lesson not yet started._
