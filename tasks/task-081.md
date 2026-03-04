# Lesson 081: Unit tests in depth - organization, helpers, test modules

## Section 18: Testing & Quality

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Organize unit tests in `#[cfg(test)] mod tests {}` blocks within each source file and understand why `#[cfg(test)]` means test code is excluded from release builds
- [ ] Write test helper functions and constructors to reduce duplication across tests, using `pub(crate)` visibility where needed
- [ ] Use setup/teardown patterns in Rust tests (helper functions called at the start of each test, RAII guards for cleanup) since Rust has no built-in `@Before`/`@After` like JUnit
- [ ] Test private functions directly from within the same module (Rust allows this, unlike Java) and understand the debate around testing private vs public interfaces
- [ ] Use `#[ignore]` for slow tests, `#[should_panic]` for expected panics, and `cargo test` filtering to run subsets of tests

## Exercises
- [ ] **Exercise 1 -- Test organization**: Create a `math_utils` module with functions `gcd(a: u64, b: u64) -> u64` and `lcm(a: u64, b: u64) -> u64`. Write a `#[cfg(test)] mod tests` block with at least 6 tests covering normal cases, edge cases (0, 1, same number), and large numbers. Add a helper function `fn assert_gcd_lcm_identity(a: u64, b: u64)` that verifies `gcd * lcm == a * b`.
- [ ] **Exercise 2 -- Testing private functions**: Create a module with a public `fn parse_and_validate(input: &str) -> Result<Config, ParseError>` that internally calls private helpers `fn parse_fields(input: &str) -> Vec<(&str, &str)>` and `fn validate_port(port: &str) -> Result<u16, ParseError>`. Write unit tests for both the private helpers and the public function. Discuss when testing privates is appropriate.
- [ ] **Exercise 3 -- Test helpers and fixtures**: Build a `UserStore` struct with `add_user`, `get_user`, `delete_user` methods. Create a `fn test_store_with_sample_data() -> UserStore` helper that populates a store with 5 test users. Write 8+ tests using this helper: test retrieval, deletion, duplicate handling, missing user errors. Use `#[should_panic]` on one test that expects a panic on invalid input.
- [ ] **Exercise 4 -- Ignore and filtering**: Add a `#[ignore]` test that performs a slow computation (e.g., compute the 40th Fibonacci number naively). Run `cargo test` and verify it is skipped. Run `cargo test -- --ignored` to run only ignored tests. Run `cargo test gcd` to filter by name. Document the cargo test CLI flags you discovered.

## Notes
_Lesson not yet started._
