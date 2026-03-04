# Lesson 021: The derive attribute - Debug, Clone, PartialEq, Eq, Hash

## Section 5: Structuring Data

## Status: pending

## Added
- Initial curriculum design [NEW - bridging lesson]

## Objectives
- [ ] Understand the `#[derive(...)]` attribute syntax and how it auto-generates trait implementations at compile time
- [ ] Use `Debug` to enable `{:?}` and `{:#?}` formatting for structs and enums, understanding this replaces Java's `toString()` and Go's `%+v`
- [ ] Use `Clone` and `Copy` to control duplication -- understand that `Copy` requires `Clone`, `Copy` is implicit duplication (like `i32`), and `Clone` is explicit (`.clone()`)
- [ ] Use `PartialEq` and `Eq` to enable `==` and `!=` comparisons, understanding the difference (PartialEq allows partial equivalence like `f64`, Eq guarantees full equivalence)
- [ ] Use `Hash` to make structs usable as `HashMap` keys, knowing that `Hash` requires `Eq` and that types with `f64` fields cannot derive `Hash`

## Exercises
- [ ] **Exercise 1 - Debug printing**: Create a `Student` struct with `name: String`, `grade: u8`, and `gpa: f64`. Derive `Debug` and print it with `println!("{:?}", s)` and `println!("{:#?}", s)`. Then create a `Classroom` struct containing a `Vec<Student>` and print the whole nested structure.
- [ ] **Exercise 2 - Clone and Copy**: Create a `Point { x: f64, y: f64 }` that derives both `Clone` and `Copy`. Verify that assignment copies instead of moves. Then create a `Label { text: String }` that derives only `Clone` (not `Copy` -- try deriving Copy and observe the compiler error explaining that String is not Copy). Practice calling `.clone()` explicitly.
- [ ] **Exercise 3 - Equality comparison**: Derive `PartialEq` on a `Coordinate { x: i32, y: i32 }` struct and use `==` and `!=` to compare instances. Then derive both `PartialEq` and `Eq`. Discuss why `f64` fields prevent deriving `Eq` (NaN != NaN violates reflexivity). Write `assert_eq!` tests comparing struct instances.
- [ ] **Exercise 4 - HashMap keys**: Create a `Tile { row: u8, col: u8 }` struct that derives `Hash`, `Eq`, and `PartialEq`. Use it as a key in a `HashMap<Tile, String>` to store tile labels. Demonstrate that forgetting any of the three derives causes a compiler error. Experiment with which combinations of derives are valid for structs containing different field types.

    > **Note**: HashMap is covered in depth in lesson 036. Here we only need `use std::collections::HashMap;` and basic `map.insert(key, value)` / `map.get(&key)` to demonstrate the Hash derive requirement.

## Notes
_Lesson not yet started._
