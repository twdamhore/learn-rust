# Lesson 019: Structs - named, tuple, unit structs

## Section 5: Structuring Data

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Define named structs with typed fields and create instances, comparing syntax with Java classes and Go structs
- [ ] Create tuple structs for lightweight wrappers (e.g., `struct Meters(f64)`) and understand when to use them vs named structs
- [ ] Understand unit structs (`struct Marker;`) and their use as zero-sized types for trait implementations
- [ ] Use field init shorthand when variable names match field names (e.g., `User { name, age }` instead of `User { name: name, age: age }`)
- [ ] Use struct update syntax (`..other_struct`) to create new instances from existing ones, and understand that this moves non-Copy fields

## Exercises
- [ ] **Exercise 1 - User model**: Define a `User` struct with `username: String`, `email: String`, `active: bool`, and `login_count: u64`. Write a function `create_user(username: String, email: String) -> User` that uses field init shorthand and returns a new active user with login_count 0. Create a second user from the first using struct update syntax and verify the original is partially moved. **Note on partial moves**: When you use struct update syntax (`..book1`), `Copy` fields (like `bool`, `u64`) are copied, while non-`Copy` fields (like `String`) are moved. After this, `book1` is partially moved -- you can still access its `Copy` fields but not the moved `String` fields, and you cannot use `book1` as a whole.
- [ ] **Exercise 2 - Tuple structs**: Create a `Color(u8, u8, u8)` tuple struct and a `Point(f64, f64, f64)` tuple struct. Write functions `is_black(c: &Color) -> bool` and `distance_from_origin(p: &Point) -> f64`. Demonstrate that `Color` and `Point` are distinct types even though they have the same field layout.
- [ ] **Exercise 3 - Rectangle**: Define a `Rectangle` struct with `width` and `height` as `f64` fields. Write a standalone function `area(rect: &Rectangle) -> f64` (methods come in lesson 020). Create several rectangles including one using struct update syntax and print their areas.
- [ ] **Exercise 4 - Comparison with Java/Go**: Take a simple Java class (e.g., a `Book` with title, author, pages) and rewrite it as a Rust struct. Note the differences: no `new` keyword, no class inheritance, fields private by default, ownership of String fields. Do the same starting from a Go struct and note the similarities (no inheritance, composition-friendly).

## Notes
_Lesson not yet started._
