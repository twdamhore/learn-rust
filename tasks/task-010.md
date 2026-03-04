# Lesson 010: Writing and running tests - #[test], assert!, cargo test

## Section 2: Language Basics

## Status: pending

## Added
- Initial curriculum design [NEW - bridging lesson]

## Objectives
- [ ] Write test functions using the `#[test]` attribute and understand that tests are functions that panic on failure
- [ ] Use `assert!`, `assert_eq!`, and `assert_ne!` macros with custom failure messages (second argument to these macros)
- [ ] Run tests with `cargo test`, filter tests by name (`cargo test test_name`), and read test output (passed/failed/ignored)
- [ ] Use `#[should_panic]` to test that a function panics, including `#[should_panic(expected = "message")]` to verify the panic message
- [ ] Organize tests in a `#[cfg(test)] mod tests { ... }` block and understand why this convention exists (conditional compilation, not included in release builds)

## Exercises
- [ ] **Exercise 1 - Test the basics**: Create a fresh project: `cargo new lesson-010 --lib && cd lesson-010`. Copy in (or rewrite) functions from lessons 5-8 (e.g., `min_max`, `add`, `divide`, `apply_twice`) and write `#[test]` functions for each. Use `assert_eq!` to verify return values. Include at least one test with a custom failure message: `assert_eq!(result, expected, "add({}, {}) should be {}", a, b, expected)`
- [ ] **Exercise 2 - Testing panics**: Write a function `divide_safe(a: i32, b: i32) -> i32` that panics with "division by zero" when `b` is 0. Write a `#[should_panic(expected = "division by zero")]` test for it. Also write a normal test that verifies it works with valid inputs
- [ ] **Exercise 3 - Test organization and filtering**: Create a `#[cfg(test)] mod tests` block with at least 4 tests (stretch: 6): some for arithmetic, some for string operations, and some edge cases. Run `cargo test`, then run only the arithmetic tests by name filter (`cargo test arithmetic`). Add a `#[ignore]` attribute to a slow or incomplete test and run it explicitly with `cargo test -- --ignored`
- [ ] **Exercise 4 - assert_ne! and boundary tests**: Write tests that use `assert_ne!` to verify that two computations produce different results. Write boundary tests: test with 0, negative numbers, `i32::MAX`, and `i32::MIN`. Observe what happens when an assertion fails and practice reading the test failure output

## Notes
_Lesson not yet started._
