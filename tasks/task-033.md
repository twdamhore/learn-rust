# Lesson 033: Testing with ownership, Result, and custom types

## Section 7: Error Handling

## Status: pending

## Added
- Initial curriculum design [NEW - bridging lesson]

## Objectives
- [ ] Write tests for functions that take ownership, borrow, or return owned data, understanding how test code interacts with the ownership system
- [ ] Test functions that return `Result<T, E>`, using both `assert!(result.is_ok())` and the `?` operator directly in test functions that return `Result`
- [ ] Test custom error types by verifying specific error variants, error messages, and error source chains
- [ ] Use `#[should_panic]` and `#[should_panic(expected = "message")]` to test code that is supposed to panic
- [ ] Organize test modules with helper/fixture functions that create test data, avoiding repetition across tests

## Exercises
- [ ] **Exercise 1 - Testing owned data**: Create a `UserProfile` struct with `name: String` and `email: String`. Write functions `create_profile()`, `update_email()`, and `merge_profiles()`. Write tests that demonstrate Rust enforces ownership at compile time: write a test showing data is correctly accessible after a move to the new owner. In a comment, note that trying to use the original variable after a move produces a compile error (the compiler, not the test runner, enforces this)
- [ ] **Exercise 2 - Testing Result paths**: Write a function `fn parse_age(input: &str) -> Result<u8, AgeError>` with custom error variants for empty input, non-numeric input, and out-of-range values (0 or >150). Write tests covering every Ok and Err path, using `assert_eq!` on error variants and test functions that return `Result<(), AgeError>`
- [ ] **Exercise 3 - Testing panics**: Write `fn divide_or_panic(a: i32, b: i32) -> i32` that panics on division by zero. Write tests using `#[should_panic]` and `#[should_panic(expected = "division by zero")]`. Also test that non-panic inputs work correctly
- [ ] **Exercise 4 - Test fixtures and helpers**: Create a test module with helper functions: `fn sample_config() -> Config`, `fn sample_config_with_errors() -> Config`, `fn assert_error_contains(result: Result<Config, ConfigError>, expected_msg: &str)`. Use these helpers across 4+ tests to verify config parsing, demonstrating DRY test organization. (Tip: You can reuse the `Config`/`ConfigError` types from lesson 031 Exercise 4 if you completed it, for cross-lesson continuity.)

## Notes
_Lesson not yet started._
