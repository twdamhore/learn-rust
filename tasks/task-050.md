# Lesson 050: Advanced lifetimes - HRTBs, variance, subtyping

## Section 10: Lifetimes

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Understand Higher-Rank Trait Bounds (HRTBs) using `for<'a>` syntax: a way to say "this works for any lifetime", which is needed when a closure or function pointer must accept references with arbitrary lifetimes
- [ ] Grasp lifetime variance conceptually: covariance (can substitute a longer lifetime where a shorter one is expected, e.g., `&'static str` for `&'a str`), contravariance (rare, in function parameter position), and invariance (`&mut T` is invariant in `T` to prevent aliasing bugs)
- [ ] Understand lifetime subtyping: `'a: 'b` means `'a` outlives `'b`, which means `&'a T` can be used wherever `&'b T` is expected (longer lifetimes are subtypes of shorter ones)
- [ ] Know when HRTBs are needed in practice: primarily when passing closures that accept references to functions like `fn apply(f: impl for<'a> Fn(&'a str) -> &'a str)` or when working with trait bounds that involve borrowed data
- [ ] Understand `PhantomData<&'a T>` as a way to tell the compiler that a struct logically borrows data with lifetime `'a` even though it does not hold an actual reference (e.g., raw pointer wrappers)

## Exercises
- [ ] **HRTB with closures**: Write a function `fn apply_to_ref<F>(f: F, data: &[String]) where F: for<'a> Fn(&'a str) -> &'a str` that applies `f` to each string in the slice. Demonstrate why `F: Fn(&str) -> &str` does not work without `for<'a>` by showing the compiler error, then fix it with the HRTB
- [ ] **Variance observation**: Create examples showing covariance in action: assign a `&'static str` to a variable of type `&'a str`. Then demonstrate invariance: try to use a `&mut &'static str` where a `&mut &'a str` is expected, and observe the compiler rejection. Explain why `&mut` must be invariant
- [ ] **PhantomData lifetime marker**: Create a struct `RawSlice<'a, T>` that wraps a raw pointer `*const T` and a length, with `PhantomData<&'a T>` to tie the struct to a lifetime. Implement a safe `from_slice()` constructor and a safe `get()` method. Show that the compiler prevents using the `RawSlice` after the original data is dropped
- [ ] **Study real-world HRTBs**: Find and annotate examples of `for<'a>` in the standard library (e.g., `str::parse` requires `FromStr`, `Iterator::for_each`). For each, explain why the HRTB is necessary and what would break without it. Write your own small example demonstrating the same pattern

## Notes
_**SUPERSEDED**: This lesson has been split into [Lesson 50a](task-050a.md) and [Lesson 50b](task-050b.md). Use those files instead._

_Lesson not yet started._
