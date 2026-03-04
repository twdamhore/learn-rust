# Lesson 026: Advanced patterns - guards, bindings, nested patterns, @

## Section 5: Structuring Data

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Use match guards (`if` conditions in match arms) to add extra conditions beyond what the pattern alone can express
- [ ] Use `@` bindings to capture a value while simultaneously testing it against a pattern (e.g., `id @ 1..=5 => ...`)
- [ ] Match on nested enums and structs, destructuring multiple levels deep in a single pattern
- [ ] Use or-patterns (`|`) to handle multiple patterns in a single match arm
- [ ] Understand pattern matching on references and the difference between `&val` pattern and matching on `ref val` (Note: `ref` in patterns is largely superseded by Rust 2018+ match ergonomics and is included here for reading older code and documentation)

## Exercises
- [ ] **Exercise 1 - Match guards for ranges**: Create a `grade_letter(score: u32) -> &'static str` function that uses match with range patterns and guards: `90..=100 => "A"`, `80..=89 => "B"`, etc. Note: `90..=100` is a **range pattern** (not a guard). A **match guard** uses `if`: `n if n > 0 => ...`. In this exercise you'll use both: range patterns for score ranges, and a match guard like `n if n <= 100 => ...` on the catch-all arm to distinguish invalid scores. Also write a function that matches a tuple `(x, y)` with guards like `(x, y) if x == y => "on diagonal"`.
- [ ] **Exercise 2 - @ bindings**: Write a function `categorize_age(age: u32) -> String` that uses `@` bindings: `child @ 0..=12 => format!("{child} is a child")`, `teen @ 13..=19 => ...`, etc. Then write a function matching an `Option<i32>` with `Some(n @ 1..=100) => ...` to both capture and range-check in one step.
- [ ] **Exercise 3 - Nested patterns**: Define a `Config` enum: `Config::Database(DbConfig)` where `DbConfig` has nested `ConnectionType::Tcp { host: String, port: u16 }` or `ConnectionType::Socket { path: String }`. Write a match that destructures through all layers in one arm: `Config::Database(DbConfig { conn: ConnectionType::Tcp { host, port }, .. }) => ...`. Use or-patterns to combine arms where appropriate.
- [ ] **Exercise 4 - Expression evaluator** [STRETCH]: Define an `Expr` enum with `Num(f64)`, `Add(Box<Expr>, Box<Expr>)`, `Mul(Box<Expr>, Box<Expr>)`, and `Neg(Box<Expr>)`. Write `fn eval(expr: &Expr) -> f64` using recursive pattern matching. Add a `fn simplify(expr: Expr) -> Expr` that uses patterns with guards to apply rules like "multiply by 0 gives 0" and "add 0 gives the other operand". This exercise brings together nested patterns, guards, `@` bindings, and recursive matching.
  > **Preview**: `Box<T>` is explained in lesson 54. Here it enables recursive types — the compiler needs a known size, and `Box` provides that by storing data on the heap.

## Notes
_Lesson not yet started._
