# Lesson 049b: Lifetime Practice Part B: Lifetime Design Patterns

## Section 10: Lifetimes

## Status: pending

## Added
- Split from original lesson 049 (v7 pacing review)

## Objectives
- [ ] Understand when to restructure code vs when to add annotations: if annotations become deeply nested or confusing, the design may need rethinking rather than more annotations
- [ ] Recognize unnecessary lifetime annotations and simplify them using Rust's lifetime elision rules
- [ ] Use `cargo clippy` to detect over-annotated lifetimes (the `needless_lifetimes` lint)
- [ ] Handle the common "cannot borrow as mutable because it is also borrowed as immutable" pattern when building cache-like structures, and understand the design strategies for resolving it

## Exercises
- [ ] **Over-annotated simplification**: Given a function with unnecessary explicit lifetime annotations on every reference (e.g., `fn process<'a, 'b, 'c>(a: &'a str, b: &'b i32, c: &'c [u8]) -> usize`), simplify by removing annotations that elision handles. Use `cargo clippy` to verify
- [ ] **Cache struct**: Build a `Cache<'a>` struct that holds a `&'a str` key and a computed `String` value. Implement a `fn get_or_compute()` method that returns the cached value or computes it. Encounter the common "cannot borrow as mutable because it is also borrowed as immutable" pattern and resolve it

  **Hint**: Resolve this by restructuring the code, not with `RefCell` (which is taught in lesson 056). Try the `contains_key` + `insert` pattern: check if the key exists first, compute the value in a local variable, then insert. This avoids holding an immutable borrow while trying to mutably borrow.

## Notes
_Lesson not yet started._
