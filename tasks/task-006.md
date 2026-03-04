# Lesson 006: Scalar types - integers, floats, bool, char, casting with as

## Section 2: Language Basics

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Know all integer types (`i8`/`u8` through `i128`/`u128`, plus `isize`/`usize`), their sizes, and when to use each (especially `usize` for indexing)
- [ ] Understand floating point types (`f32`, `f64`), default type inference (`f64`), and IEEE 754 pitfalls (e.g., `0.1 + 0.2 != 0.3`)
- [ ] Use `bool` and `char` types, understanding that `char` is a 4-byte Unicode scalar value (not a single byte like Java's `char` or Go's `byte`)
- [ ] Apply Rust's type inference and understand when explicit type annotations are needed (e.g., `let x: i32 = 5;` vs `let x = 5_i32;` vs suffix notation)
- [ ] Cast between numeric types using `as`, understand truncation and sign-extension behavior, and know that Rust does not implicitly convert types (unlike Java's widening)
- [ ] Understand integer overflow behavior: panic in debug mode, wrapping in release mode, and explicit methods (`wrapping_*`, `checked_*`, `saturating_*`, `overflowing_*`) (awareness-level — know these exist; no need to memorize)

## Exercises
- [ ] **Exercise 1 - Type inference explorer**: Declare variables without type annotations and use `std::any::type_name` (or deliberate type errors) to discover what types Rust infers. Test: an untyped integer literal, a float literal, a `bool`, and a `char` literal
- [ ] **Exercise 2 - Overflow behavior**: Write a program that adds 1 to `u8::MAX`. Run it in debug mode (`cargo run`) and observe the panic. Then run it in release mode (`cargo run --release`) and observe the wrapping. Rewrite using `checked_add`, `wrapping_add`, and `saturating_add` to handle overflow explicitly
- [ ] **Exercise 3 - Casting chain**: Write a function that takes an `i32`, casts it to `i8` (observing truncation), then to `u8` (observing sign reinterpretation), then to `f64`. Print each intermediate value. Test with positive, negative, and out-of-range inputs
- [ ] **Exercise 4 - Char and Unicode**: Create `char` variables for an ASCII letter, an emoji, and a CJK character. Print each with `println!` and also print their Unicode code points using `as u32`. Verify that `std::mem::size_of::<char>()` is 4 bytes

## Notes
_Lesson not yet started._
