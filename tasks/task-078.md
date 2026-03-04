# Lesson 078: Newtype pattern, type aliases, zero-sized types

## Section 17: Advanced Type System

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Use the newtype pattern to create type-safe wrappers (e.g., `Meters(f64)` vs `Kilometers(f64)`) that prevent accidental mixing of units at compile time
- [ ] Implement foreign traits on foreign types by wrapping them in newtypes -- the "orphan rule workaround"
- [ ] Create type aliases with `type` and understand that aliases are transparent (no type safety) vs newtypes which are opaque (full type safety)
- [ ] Understand zero-sized types (ZSTs) like `()`, `PhantomData<T>`, and empty structs -- why they exist, that they have zero runtime cost, and how the compiler optimizes them away
- [ ] Use `PhantomData` to express type relationships without storing data (e.g., marking a struct as owning a `T` or being covariant/invariant over a lifetime)

## Exercises
- [ ] **Exercise 1 -- Units of measure**: Create `Meters(f64)`, `Kilometers(f64)`, and `Seconds(f64)` newtypes. Implement `Add` for same-unit addition, a `to_kilometers()` method on `Meters`, and a `Speed` newtype computed from `Kilometers` and `Seconds`. Verify that `Meters + Kilometers` does not compile without explicit conversion.
- [ ] **Exercise 2 -- Display on a newtype**: Create a `Username(String)` newtype. Implement `Display` to show the username, `From<String>` and `From<&str>` for construction, and `Deref<Target=str>` so string methods work transparently. Discuss the tradeoff of implementing `Deref` on newtypes.
- [ ] **Exercise 3 -- Type aliases for complex types**: Define `type Result<T> = std::result::Result<T, AppError>` for a custom error type. Also create `type Callback = Box<dyn Fn(i32) -> i32>`. Write functions using these aliases and verify they work identically to the expanded types. Show that you CAN accidentally pass a `Result<T, OtherError>` where `type Result<T>` is expected (because aliases are transparent).
- [ ] **Exercise 4 -- ZSTs and PhantomData**: Create a `Tagged<T, Tag>` struct where `Tag` is a ZST marker (`struct Verified;` / `struct Unverified;`). The struct holds a `T` value and a `PhantomData<Tag>`. Write a function that only accepts `Tagged<String, Verified>`. Confirm with `std::mem::size_of` that `Tagged<String, Verified>` is the same size as `String`.

## Notes
_Lesson not yet started._
