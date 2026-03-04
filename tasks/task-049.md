# Lesson 049: Lifetime elision rules, function lifetimes

## Section 10: Lifetimes

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Know the three lifetime elision rules: (1) each reference parameter gets its own lifetime, (2) if there is exactly one input lifetime it is assigned to all output lifetimes, (3) if one parameter is `&self` or `&mut self`, its lifetime is assigned to all output lifetimes
- [ ] Recognize when the compiler can infer lifetimes without annotations (all three rules applied successfully cover all output lifetimes) and when explicit annotations are required (rules leave output lifetimes ambiguous)
- [ ] Write functions where elision is sufficient and understand which rule(s) apply -- building intuition for when you do and do not need to annotate
- [ ] Understand method lifetime elision (rule 3): methods that take `&self` and return a reference automatically tie the return lifetime to `self`, which is usually correct but occasionally needs overriding
- [ ] Know when explicit annotations are required despite elision rules: multiple input references with a returned reference, or when the return lifetime should not follow the default elision

## Exercises
- [ ] **Elision rule identification**: For each of these signatures, state which elision rules apply and what the fully-expanded lifetime annotations would be: (a) `fn first(s: &str) -> &str`, (b) `fn push_str(&mut self, s: &str)`, (c) `fn get(&self, key: &str) -> &str`, (d) `fn combine(a: &str, b: &str) -> &str` (does not compile)
- [ ] **Methods with &self**: Create a struct `Excerpt { text: String, start: usize, end: usize }` and implement methods `fn content(&self) -> &str` (returns a slice of `text`) and `fn with_prefix(&self, prefix: &str) -> String` (returns owned). Verify that `content()` compiles without lifetime annotations (rule 3) and explain why `with_prefix()` does not need them either (returns owned data)
- [ ] **Adding unnecessary lifetimes**: Take 3 functions that compile with elision and add explicit lifetime annotations. Verify they still compile. Then use `cargo clippy` to see if Clippy warns about unnecessary lifetime annotations (`clippy::needless_lifetimes`)
- [ ] **Elision failure case**: Write a struct with two string fields and a method `fn longer(&self, other: &Self) -> &str` that returns the longer of a field from `self` vs `other`. Observe that elision assigns the return lifetime to `&self` per rule 3, but this may be incorrect if `other` lives shorter. Add correct explicit annotations

## Notes
_Lesson not yet started._
