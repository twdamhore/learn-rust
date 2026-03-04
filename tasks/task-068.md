# Lesson 068: Declarative macros - macro_rules!, matchers, repetition

## Section 15: Macros

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Write `macro_rules!` macros with basic matchers and understand the invocation syntax
- [ ] Understand the available fragment specifiers: `expr`, `ident`, `ty`, `tt`, `literal`, `pat`, `path`, `stmt`, `block`, and when to use each
- [ ] Use repetition patterns (`$( ... )*`, `$( ... )+`, `$( ... ),*`) to handle variable numbers of arguments
- [ ] Understand macro hygiene in Rust -- why macro-generated variables do not collide with caller variables
- [ ] Use `cargo expand` (via `cargo-expand` crate) to inspect macro expansion output

## Exercises
- [ ] **Custom vec macro**: Write a `my_vec!` macro that accepts a comma-separated list of expressions and creates a `Vec` by calling `push` for each element; test with `my_vec![1, 2, 3]` and verify it equals `vec![1, 2, 3]`
- [ ] **Function generator macro**: Write a `make_adder!` macro that takes an identifier and a number, and generates a function with that name which adds the number to its argument; e.g., `make_adder!(add_five, 5)` generates `fn add_five(x: i32) -> i32 { x + 5 }`
- [ ] **Variadic print macro**: Write a `debug_print!` macro that takes any number of expressions, and for each one prints the expression text (using `stringify!`) and its value; e.g., `debug_print!(1+2, "hello".len())` prints `1+2 = 3` and `"hello".len() = 5`
- [ ] **Expand and inspect**: Install `cargo-expand` and run it on your macros from the previous exercises; study the expanded output and write comments in your code explaining any surprises in the expansion

## Notes
> **Setup**: `cargo-expand` requires the nightly toolchain. Install it with: `rustup toolchain install nightly` and then `cargo install cargo-expand`. Run with: `cargo +nightly expand`

_Lesson not yet started._
