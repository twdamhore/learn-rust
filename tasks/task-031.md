# Lesson 031: Panic, unwrap, expect, when to panic

## Section 7: Error Handling

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Understand the `panic!` macro and how stack unwinding works (vs abort), including how Rust cleans up resources on panic
- [ ] Use `unwrap()` and `expect()` on `Option` and `Result`, and understand the difference in error messages they produce
- [ ] Know when panicking is appropriate: unrecoverable errors, violated invariants, prototyping, and tests
- [ ] Configure `panic = 'abort'` in `Cargo.toml` and understand the trade-off (binary size vs cleanup)
- [ ] Compare Rust's panic model with Java's unchecked exceptions and Go's `panic`/`recover` mechanism

## Exercises
- [ ] **Exercise 1 - Trigger panics**: Write code that panics via array out-of-bounds access, `unwrap()` on `None`, and an explicit `panic!("message")` call. Run each and read the backtrace (`RUST_BACKTRACE=1`)
- [ ] **Exercise 2 - unwrap vs expect**: Create a function that parses a string to an integer. Call it with valid and invalid input using both `unwrap()` and `expect("context message")`. Compare the panic output and explain why `expect` is preferred
- [ ] **Exercise 3 - Intentional panic with guard**: Write a `fn divide(a: i32, b: i32) -> i32` that panics with a descriptive message when `b == 0`. Call it from `main` and verify the message appears in the output
- [ ] **Exercise 4 - Panic abort mode**: Set `[profile.dev] panic = 'abort'` in `Cargo.toml`, trigger a panic, and observe that the backtrace is different (no unwinding). Revert the setting afterward and note when abort mode is useful (embedded, binary size)
- [ ] **Stretch Activity - `catch_unwind`** [STRETCH]: Experiment with `std::panic::catch_unwind` to recover from a panic. Note that this is rarely used in normal Rust code — it exists mainly for FFI boundaries and test harnesses.
  ```rust
  use std::panic;

  fn main() {
      let result = panic::catch_unwind(|| {
          panic!("oh no!");
      });
      println!("Caught panic: {:?}", result);
  }
  ```

## Notes
_Lesson not yet started._

> **Supplementary reading**: If you finish early, read [The Rust Programming Language, Chapter 9.1 - Unrecoverable Errors with panic!](https://doc.rust-lang.org/book/ch09-01-unrecoverable-errors-with-panic.html) for additional context on panic behavior, stack unwinding, and abort mode.
