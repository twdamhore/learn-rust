# Lesson 054: Variance and Subtyping

## Section 10: Lifetimes

## Status: pending

## Added
- Split from original lesson 053 (v6 pacing review)

## Objectives
- [ ] Understand covariance, contravariance, and invariance at an awareness level: these describe how subtyping relationships between types change when those types are used inside other types (e.g., inside references, mutable references, function arguments)
- [ ] Know that `&'a T` is covariant in `'a`: a longer lifetime can be used where a shorter one is expected (e.g., `&'static str` can be used where `&'a str` is expected), because it's always safe to use a reference that lives longer
- [ ] Understand why `&mut T` is invariant: if `&mut &'static str` could be used where `&mut &'a str` is expected, you could write a short-lived reference through it, corrupting the `'static` guarantee. Invariance prevents this aliasing bug.
- [ ] Recognize when variance matters in practice: primarily when working with mutable references to references, generic type parameters, and (later) when using `PhantomData` to control variance in custom types

## Exercises
- [ ] **Demonstrate covariance**: Write a function `fn print_str(s: &str)` and call it with a `&'static str` (a string literal). Then write a function `fn pick_first<'a>(a: &'a str, b: &'a str) -> &'a str` and call it with one `&'static str` and one local `&'a str`. Observe how the compiler shortens the `'static` lifetime to match -- this is covariance in action. Add comments explaining why this is safe.
- [ ] **Demonstrate invariance**: Write a function that takes `&mut &str` and tries to assign a locally-scoped string reference through it. Observe the compiler error. Then try to pass a `&mut &'static str` where `&mut &'a str` is expected and observe the rejection. Write comments explaining why `&mut` must be invariant to prevent dangling references.
- [ ] **(Optional) Rustonomicon summary**: Read the [Rustonomicon chapter on variance](https://doc.rust-lang.org/nomicon/subtyping.html) and write a comment block summarizing: (a) what is covariant, contravariant, and invariant in Rust's type system, (b) the variance of `&'a T`, `&'a mut T`, `fn(T)`, `Cell<T>`, and (c) why `Vec<T>` is covariant in `T` but `Cell<T>` is invariant.

## Notes
- This lesson is at **awareness level**, not mastery. Variance is a topic even experienced Rustaceans revisit. The goal is to recognize when variance is relevant and have a mental model, not to memorize the full variance table.
- Raw pointer / unsafe exercises from the original lesson 053 were removed (prerequisite violation -- unsafe not taught until lesson 73).
- PhantomData exercises were removed (covered in lesson 062).
_Lesson not yet started._
