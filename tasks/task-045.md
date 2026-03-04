# Lesson 045: Operator overloading, Deref/DerefMut, Drop

## Section 9: Generics & Traits

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Overload operators by implementing traits from `std::ops` (`Add`, `Sub`, `Mul`, `Neg`, `Index`, etc.) and understand that operator overloading in Rust is just trait implementation -- no magic syntax
- [ ] Implement `Deref` and `DerefMut` to make custom types behave like smart pointers, enabling automatic dereferencing when calling methods or passing to functions
- [ ] Understand deref coercion: how `&MyType` automatically coerces to `&Target` when `MyType` implements `Deref<Target = Target>`, and the coercion chain (e.g., `&String` -> `&str` -> `&[u8]`)
- [ ] Implement the `Drop` trait for custom cleanup logic (like Java's try-with-resources or Go's defer), understanding that `drop()` is called automatically when a value goes out of scope
- [ ] Understand the mutual exclusion between `Drop` and `Copy`: a type cannot implement both because `Copy` means bitwise duplication (no custom cleanup), while `Drop` means the value has cleanup logic that must run exactly once

## Exercises
- [ ] **Vector2D arithmetic**: Create a `Vector2D { x: f64, y: f64 }` struct. Start with `Add` (vector addition) and `Neg` (negate both components). Write tests verifying `v1 + v2` and `-v1` work correctly. If time permits, also implement `Sub` (vector subtraction) and `Mul<f64>` (scalar multiplication) as additional practice
- [ ] **Custom smart pointer**: Create a `MyBox<T>` struct that wraps a value. Implement `Deref<Target = T>` for it. Demonstrate deref coercion by writing a function `fn hello(name: &str)` and calling it with `&MyBox<String>` -- observe the automatic chain `&MyBox<String>` -> `&String` -> `&str`
- [ ] **Deref coercion chain [STRETCH]**: Create a `CaseInsensitiveString` wrapper around `String` that implements `Deref<Target = str>`. Show that you can call `&str` methods like `.len()`, `.contains()`, and `.to_uppercase()` directly on `CaseInsensitiveString` without unwrapping
- [ ] **Drop for resource tracking**: Create a `DatabaseConnection` struct that prints "Connection opened to {name}" on creation and implements `Drop` to print "Connection to {name} closed". Create several connections in nested scopes and observe the drop order (LIFO). Then try calling `std::mem::drop()` to drop a connection early

- [ ] **Exercise 5 — Drop and Copy are mutually exclusive** (5 min): Try adding `#[derive(Copy, Clone)]` to the `DatabaseConnection` struct from Exercise 4. Read the compiler error. Why can't a type implement both `Drop` and `Copy`? Write a one-line comment explaining the reason.

## Notes
_Lesson not yet started._
