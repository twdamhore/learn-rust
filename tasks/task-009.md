# Lesson 009: Control flow - if/else, loop, while, for, labels, break with values

## Section 2: Language Basics

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Use `if`/`else` as expressions that return values (assign the result of an `if` to a variable) - contrast with Java/Go where `if` is only a statement
- [ ] Understand `loop` (infinite loop with `break`), `while` (conditional loop), and `for` (iterator-based loop), and know which is idiomatic for each situation
- [ ] Use loop labels (`'label: loop { ... }`) to name nested loops, and `break 'label` / `continue 'label` to control which loop is affected
- [ ] Return values from `loop` using `break value` - a unique Rust feature not found in Java or Go
- [ ] Use `for` with ranges (`1..=10`), iterators (`.iter()`, `.enumerate()`), and understand why `for` is preferred over manual indexing in Rust

## Exercises
- [ ] **Exercise 1 - if as expression**: Write a program that assigns a variable using `let status = if score >= 60 { "pass" } else { "fail" };`. Extend it to a multi-branch version using `else if` for letter grades (A/B/C/D/F). Verify that all branches must return the same type
- [ ] **Exercise 2 - Loop with break value**: Use `loop` to simulate a retry mechanism: start a counter at 0, increment it each iteration, and `break counter` when it reaches a target. Assign the result of the `loop` to a variable and print it. This pattern is useful for search loops
- [ ] **Exercise 3 - Nested loops with labels**: Write a program with two nested loops (outer labeled `'outer`). The inner loop should search for a condition and `break 'outer` when found. Example: find the first pair `(i, j)` where `i * j == 42` with both `i` and `j` ranging from 1 to 20
- [ ] **Exercise 4 - FizzBuzz**: Implement FizzBuzz (1-100) using a `for` loop with a range. Print "Fizz" for multiples of 3, "Buzz" for multiples of 5, "FizzBuzz" for multiples of both, and the number otherwise. Then rewrite it using `match` with tuple pattern `(n % 3, n % 5)` (preview of lesson 23 — just follow the pattern shown)

  > **Match with tuple pattern** template:
  > ```rust
  > match (n % 3, n % 5) {
  >     (0, 0) => println!("FizzBuzz"),
  >     (0, _) => println!("Fizz"),
  >     (_, 0) => println!("Buzz"),
  >     _ => println!("{}", n),
  > }
  > ```
  > This previews pattern matching from lesson 025 -- just follow the syntax for now.
- [ ] **Exercise 5 - Number guessing loop** [OPTIONAL]: Write a loop that reads a hardcoded "secret" number. Use a mutable counter to simulate guesses (e.g., incrementing by 7 each iteration). Break when the guess matches or exceeds the secret. Print the number of attempts. (Full interactive version will come after we cover I/O and Result)

## Notes
_Lesson not yet started._
