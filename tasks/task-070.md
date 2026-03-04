# Lesson 070: Advanced macro_rules! - TT munching, push-down accumulation

## Section 15: Macros

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Understand the TT (token tree) munching pattern -- recursively consuming tokens one at a time to build complex output
- [ ] Understand push-down accumulation -- passing an accumulator through recursive macro calls to build up the result
- [ ] Build recursive macros that process variable-length input by matching the first token(s) and recursing on the rest
- [ ] Use internal macro rules (prefixed with `@`) as helper arms for multi-phase macro expansion -- the `@` prefix is a community convention (not special syntax) that prevents external callers from reaching internal helper rules; e.g., `(@acc [$($reversed:expr),*] $first:expr, $($rest:expr),*) => { ... }`
- [ ] Understand macro limitations: no runtime information, limited type introspection, lack of mutable state across invocations

## Exercises
- [ ] **Counting macro**: Implement a `count!` macro using TT munching that counts the number of token trees passed to it; e.g., `count!(a b c d)` evaluates to `4`; use a recursive approach that peels off one `$tt:tt` at a time
- [ ] **Recursive type builder**: Write a macro `nested!` that generates nested `Option` types; e.g., `nested!(3, i32)` expands to `Option<Option<Option<i32>>>`; use recursion with a base case at 0
- [ ] **Push-down accumulation**: Write a `reverse!` macro that takes a list of expressions and produces them in reverse order as a tuple; e.g., `reverse!(1, 2, 3)` produces `(3, 2, 1)`; use an internal `@acc` rule that accumulates items
  Hint: `reverse!(1, 2, 3)` should expand to `reverse!(@acc [] 1, 2, 3)` where `@acc` is the internal helper rule and `[]` is the accumulator. Each recursive step moves one item from the input to the accumulator.
- [ ] **Simple DSL [STRETCH]**: Implement a `calc!` DSL macro that supports basic arithmetic in a readable syntax; e.g., `calc!(add 2 to 3)` returns `5`, `calc!(mul 4 by 3)` returns `12`; use TT munching to parse the keyword-based syntax

## Notes
_Lesson not yet started._
