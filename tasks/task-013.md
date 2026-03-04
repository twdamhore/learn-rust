# Lesson 013: Copy vs Clone, when moves happen

## Section 3: Ownership System

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Understand the `Copy` trait: types that implement it are duplicated bit-for-bit on assignment instead of moved - includes all integer types, `bool`, `char`, `f32`/`f64`, and tuples/arrays of Copy types
- [ ] Understand the `Clone` trait: provides an explicit `.clone()` method for deep copying - every `Copy` type also implements `Clone`, but not vice versa
- [ ] Know when to `#[derive(Copy, Clone)]` on custom structs - the struct must contain only Copy fields; deriving Copy on a struct with a String field is a compile error
- [ ] Understand the relationship: `Copy` is a marker trait (no method), `Clone` has `.clone()`, and `Copy: Clone` (Copy requires Clone as a supertrait)
- [ ] Recognize all the situations where moves happen and decide whether to restructure code, use references, or clone

## Exercises
- [ ] **Derive Copy+Clone**: Create a `struct Point { x: f64, y: f64 }` and derive `Copy` and `Clone`. Assign it to another variable and verify both are usable. Then create `struct Label { name: String, point: Point }` and try to derive Copy - read and understand the error, then derive only Clone
- [ ] **Explicit clone**: Create a `String`, call `.clone()` to create a deep copy, modify the clone, and verify the original is unchanged. Then create a `Vec<String>`, clone it, push to the clone, and verify the original Vec is unmodified
- [ ] **When moves happen**: Write a function that takes a `Vec<i32>` by value and a function that takes a `Vec<String>` by value. In each case, try to use the original after the call. For the String version, fix it three ways: (1) clone before passing, (2) have the function return the Vec back, (3) pass a reference instead (preview of lesson 014)
- [ ] **Copy semantics deep dive**: Create an array `[i32; 5]` and assign it - verify both arrays work (Copy). Create a `[String; 3]` using `std::array::from_fn` and try to assign it - observe the move. Write comments explaining why fixed-size arrays of Copy types are Copy but arrays of non-Copy types are not

  > **Note**: `std::array::from_fn` is a standard library helper — you can also just write the array elements explicitly if the syntax feels unfamiliar.

## Notes
_Lesson not yet started._
