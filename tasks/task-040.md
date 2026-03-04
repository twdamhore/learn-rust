# Lesson 040: Traits - defining, implementing, default methods

## Section 9: Generics & Traits

## Status: pending

## Added
- Initial curriculum design

> **Note**: You've already used traits informally — `impl Display` in lesson 31 and `impl Iterator` in lesson 38. This lesson formalizes what you've been doing.

## Objectives
- [ ] Define traits with required method signatures and implement them for custom types using `impl TraitName for TypeName` blocks
- [ ] Provide default method implementations in trait definitions that implementors can use as-is or override, understanding when defaults make sense
- [ ] Understand trait coherence and the orphan rule: you can only implement a trait for a type if either the trait or the type is local to your crate -- attempt a violation and read the error
- [ ] Compare Rust traits (explicit `impl`, checked at compile time) with Java interfaces (explicit `implements`, checked at compile time) and Go interfaces (implicit satisfaction, checked at runtime for interface values)
- [ ] Use traits to define shared behavior across unrelated types and call trait methods on different concrete types through a common interface

## Exercises
- [ ] **Exercise 1 - Summary trait**: Define a `Summary` trait with a required method `fn summarize(&self) -> String` and a default method `fn preview(&self) -> String` that returns the first 50 characters of `summarize()`. Implement `Summary` for `NewsArticle` (title + author + location) and `Tweet` (username + content, truncated)
- [ ] **Exercise 2 - Default method override**: Extend the `Summary` trait to have a default `fn read_time(&self) -> usize` that estimates reading time from `summarize().len()`. Override it on one type to provide a more accurate calculation, and leave the default on another type
- [ ] **Exercise 3 - Orphan rule experiment**: Try to implement `std::fmt::Display` for `Vec<i32>` -- read and understand the compiler error about the orphan rule. Then fix it by creating a newtype wrapper `struct Wrapper(Vec<i32>)` and implementing `Display` on the wrapper
- [ ] **Exercise 4 - Trait for multiple types**: Define a `Drawable` trait with `fn draw(&self)` and `fn bounding_box(&self) -> (f64, f64, f64, f64)`. Implement it for `Circle`, `Rectangle`, and `Triangle` structs, then write a function that takes any `Drawable` and prints its bounding box. Use `impl Drawable` or `fn draw_all<T: Drawable>(items: &[T])` -- trait objects (`dyn Drawable`) are covered in lesson 043.

## Notes
_Lesson not yet started._
