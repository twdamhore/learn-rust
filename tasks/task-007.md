# Lesson 007: Compound types - tuples, arrays, ranges

## Section 2: Language Basics

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Create tuples with mixed types, access elements with dot notation (`.0`, `.1`), and destructure tuples into individual variables
- [ ] Understand the unit tuple `()` as Rust's "void" equivalent (contrast with Java's `void` and Go's empty return)
- [ ] Create fixed-size arrays with `[T; N]` syntax, understand that size is part of the type, and access elements with indexing (with runtime bounds checking that panics on out-of-bounds)
- [ ] Use ranges (`..`, `..=`, `a..b`, `a..=b`) in for loops and for slicing, understanding inclusive vs exclusive bounds
- [ ] Contrast Rust arrays with Java arrays (fixed-size, same-type, stack-allocated) and Go slices (Rust arrays are closer to Go's `[N]T` arrays, not slices)

## Exercises
- [ ] **Exercise 1 - Tuple gymnastics**: Write a function `min_max(a: i32, b: i32, c: i32) -> (i32, i32)` that returns the minimum and maximum of three numbers as a tuple. Call it and destructure the result. Also try nested tuples: create a tuple of tuples and access a deeply nested element
- [ ] **Exercise 2 - Array operations**: Create an array of 5 integers. Print it with `{:?}`. Access each element by index. Deliberately try accessing an out-of-bounds index and observe the panic message. Then create an array initialized with `[0; 10]` (ten zeros) and print its length with `.len()`
- [ ] **Exercise 3 - Range iteration**: Write a program that uses `for i in 1..=100` to print numbers 1-100 but replaces multiples of 5 with "buzz". Then use a range to take a slice of an array: `let slice = &arr[1..4];` and print the slice
- [ ] **Exercise 4 - Multi-value return**: Write a function `analyze_array(arr: [f64; 5]) -> (f64, f64, f64)` that returns the sum, minimum, and maximum of a 5-element array. Destructure the result and print each value with labels

## Notes
_Lesson not yet started._
