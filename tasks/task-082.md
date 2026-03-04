# Lesson 082: Integration tests, test fixtures, conditional compilation

## Section 18: Testing & Quality

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Set up the `tests/` directory for integration tests and understand how each file in `tests/` is compiled as a separate crate that can only access the library's public API
- [ ] Create shared test utility modules in `tests/common/mod.rs` and use them across multiple integration test files
- [ ] Use conditional compilation with `#[cfg(test)]`, `#[cfg(feature = "...")]`, and `#[cfg(target_os = "...")]` to include test-only code and feature-gated tests
- [ ] Understand the difference between unit tests (test internals, in `src/`) and integration tests (test public API, in `tests/`) and when to use each
- [ ] Test error conditions and edge cases from an external user's perspective, verifying that the public API returns correct error types

## Exercises
- [ ] **Exercise 1 -- Integration test setup**: Create a small library crate with a public API for a `Calculator` struct (methods: `new()`, `add()`, `subtract()`, `multiply()`, `divide() -> Result`). Write integration tests in `tests/calculator_tests.rs` that test the public API end-to-end, including error handling for divide-by-zero. Confirm that private helper functions are NOT accessible from integration tests.
- [ ] **Exercise 2 -- Shared test utilities**: Create `tests/common/mod.rs` with helper functions (e.g., `setup_temp_dir() -> TempDir`, `create_test_file(dir: &Path, name: &str, content: &str)`). Use these helpers in two separate integration test files (`tests/read_tests.rs` and `tests/write_tests.rs`) that test a file-processing library. Verify both test files can share the common module.
- [ ] **Exercise 3 -- Feature-gated tests**: Add a `verbose` feature to your library's `Cargo.toml` (`[features] default = [] verbose = []`). Write a `#[cfg(feature = "verbose")] fn log_detail(msg: &str) { println!("[VERBOSE] {}", msg); }` helper and call it from library functions. Write `#[cfg(feature = "verbose")]` tests that verify verbose output is produced. Write `#[cfg(not(feature = "verbose"))]` tests that verify the library works without verbose logging. Run `cargo test`, `cargo test --features verbose`, and `cargo test --all-features` to see the differences.
- [ ] **Exercise 4 -- Error condition testing**: For the calculator library, write integration tests that exhaustively test error conditions: division by zero, overflow for large numbers, and invalid operations. Use `matches!` macro to assert specific error variants. Write a test that verifies the `Display` implementation on your error type produces human-readable messages.

## Notes
_Lesson not yet started._
