# Lesson 022: Enums - basic, with data, Option<T>

## Section 5: Structuring Data

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Define basic C-style enums with named variants and understand they can be cast to integers with `as`
- [ ] Create enums with data attached to variants (tuple variants like `V4(u8,u8,u8,u8)` and struct variants like `Move { x: i32, y: i32 }`)
- [ ] Understand `Option<T>` -- Rust's replacement for null -- and why the language has no null values, comparing with Java's `Optional<T>` and Go's zero-value approach
- [ ] Use core `Option` methods: `unwrap()`, `expect()`, `unwrap_or()`, `unwrap_or_else()`, `is_some()`, `is_none()`, `map()`, and `and_then()`
- [ ] Compare Rust enums (algebraic data types / tagged unions) with Java enums (fixed set of constants) and Go's `iota` pattern (untyped integer constants), noting that Rust enums are far more powerful

## Exercises
- [ ] **Exercise 1 - IP address enum**: Define an `IpAddr` enum with `V4(u8, u8, u8, u8)` and `V6(String)` variants. Write a function `display_addr(addr: &IpAddr) -> String` that formats each variant appropriately. Create several addresses and display them. Note how this differs from the approach in Java (separate classes or subclasses) and Go (interface with two struct implementations).
- [ ] **Exercise 2 - Message enum**: Create a `Message` enum with four variants: `Quit` (no data), `Echo(String)`, `Move { x: i32, y: i32 }`, and `ChangeColor(u8, u8, u8)`. Write a function `process_message(msg: Message)` that prints what each message does. This demonstrates mixing unit, tuple, and struct variants in one enum.
- [ ] **Exercise 3 - Option fundamentals**: Write a function `find_first_even(numbers: &[i32]) -> Option<i32>` that returns the first even number or `None`. Call it with various inputs and use `unwrap_or(0)`, `is_some()`, and `map(|n| n * 2)` on the result. Rewrite a Java-style null check pattern (`if (result != null) { use(result); }`) using `Option` and `if let`. Use `if let Some(value) = option { ... }` to extract the value -- this is Rust's equivalent of Java's `if (obj != null)`. Full coverage of `if let` comes in lesson 023.
- [ ] **Exercise 4 - Option chaining** [STRETCH]: Write a function `get_username_length(db: &HashMap<u32, String>, id: u32) -> Option<usize>` that looks up a user by ID and returns the length of their name using `map()`. Then write `get_first_char(db: &HashMap<u32, String>, id: u32) -> Option<char>` using `and_then()` with `String::chars().next()`. Demonstrate chaining multiple Option operations without any unwrap calls.

## Notes
_Lesson not yet started._
