# Lesson 041: Generic functions and structs

## Section 9: Generics & Traits

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Write generic functions with one or more type parameters (`fn foo<T>(x: T)`) and understand how the compiler monomorphizes them into concrete versions (zero-cost abstraction)
- [ ] Create generic structs (`Point<T>`) and enums (`Either<L, R>`) with type parameters, and implement methods on them using `impl<T>`
- [ ] Use multiple type parameters in a single function or struct (`Pair<T, U>`) and understand when multiple parameters are needed vs a single parameter
- [ ] Compare Rust generics (monomorphization, no runtime cost) with Java generics (type erasure, boxing) and Go generics (stenciling/dictionaries), recognizing the trade-offs in compile time and binary size
- [ ] Understand the turbofish syntax (`::<Type>`) for specifying generic types when the compiler cannot infer them

## Exercises
- [ ] **Exercise 1 - Generic max function**: Write a generic `fn largest<T>(list: &[T]) -> &T` that returns the largest item in a slice -- observe the compiler error about missing trait bounds, then fix it by adding `PartialOrd` (preview of lesson 043)
- [ ] **Exercise 2 - Generic Point struct**: Create a `Point<T>` struct with `x: T` and `y: T` fields, implement a `new()` associated function and a method that returns a reference to `x`, then test it with `Point<i32>`, `Point<f64>`, and `Point<String>`
- [ ] **Exercise 3 - Mixed-type Pair**: Create a `Pair<T, U>` struct where `T` and `U` can be different types, implement a `mixup()` method that takes another `Pair` and returns a new `Pair` combining fields from both (like the Book example), and verify it works with `Pair<i32, String>` mixed with `Pair<f64, char>`
- [ ] **Exercise 4 [OPTIONAL] - Monomorphization investigation**: Write a generic function used with 3 different concrete types, compile with `cargo build --release`, and use `cargo nm` or `nm` to observe that the compiler generated separate functions for each type (confirming zero-cost monomorphization). *Note: `nm` may not be available on all systems (it is a Unix/Linux binary inspection tool). If you cannot run it, the key takeaway is that Rust monomorphizes generics -- the compiler generates a separate copy of the function for each concrete type used, resulting in zero runtime overhead but increased binary size.*

## Notes
_Lesson not yet started._
