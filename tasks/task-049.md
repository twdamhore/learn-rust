# Lesson 049: Lifetime practice - common errors, fixing lifetime puzzles

## Section 10: Lifetimes

## Status: pending

## Added
- Initial curriculum design [NEW - bridging lesson]

## Objectives
- [ ] Diagnose common lifetime error patterns by reading compiler messages carefully: "borrowed value does not live long enough", "lifetime mismatch", "cannot infer an appropriate lifetime", and "returns a reference to data owned by the current function"
- [ ] Develop strategies for fixing lifetime errors: extend the scope of the borrowed data, restructure code to avoid the borrow, return owned data instead of a reference, or use `clone()` as a deliberate trade-off
- [ ] Understand when to restructure code vs when to add annotations: if annotations become deeply nested or confusing, the design may need rethinking rather than more annotations
- [ ] Build intuition for when references are the right tool and when owned data (`String` instead of `&str`, `Vec<T>` instead of `&[T]`) simplifies the design without meaningful performance cost
- [ ] Practice reading complex lifetime error messages from the compiler and translating them into actionable fixes

## Exercises
- [ ] **Lifetime puzzle set (5 broken programs)**: Fix each of these programs that fail to compile due to lifetime issues: (1) a function returning `&str` that was created inside the function, (2) a struct holding `&str` that outlives the source `String`, (3) a method returning a reference where the borrow checker cannot determine the lifetime, (4) two structs with cross-references that create lifetime conflicts, (5) a closure capturing a reference that does not live long enough
- [ ] **Borrowed-to-owned refactor**: Take a `Tokenizer<'a>` struct that borrows a `&'a str` source and produces `Token<'a>` values (also borrowing). Refactor it to an owned `Tokenizer` that takes `String` and produces `Token` values with `String` fields. Compare the API complexity and discuss when each approach is preferable
- [ ] **Over-annotated simplification**: Given a function with unnecessary explicit lifetime annotations on every reference (e.g., `fn process<'a, 'b, 'c>(a: &'a str, b: &'b i32, c: &'c [u8]) -> usize`), simplify by removing annotations that elision handles. Use `cargo clippy` to verify
- [ ] **Cache struct**: Build a `Cache<'a>` struct that holds a `&'a str` key and a computed `String` value. Implement a `fn get_or_compute()` method that returns the cached value or computes it. Encounter the common "cannot borrow as mutable because it is also borrowed as immutable" pattern and resolve it

## Notes
_**SUPERSEDED**: This lesson has been split into [Lesson 49a](task-049a.md) and [Lesson 49b](task-049b.md). Use those files instead._

_Lesson not yet started._
