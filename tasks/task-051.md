# Lesson 051: Closures - syntax, capturing, Fn/FnMut/FnOnce

## Section 11: Closures & Functional Patterns

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Write closures using `|args| body` syntax with explicit and inferred parameter types, and store them in variables
- [ ] Understand how closures capture variables from their environment: by shared reference (`&T`), by mutable reference (`&mut T`), and by value (move)
- [ ] Distinguish the three closure traits `Fn`, `FnMut`, and `FnOnce` and explain when each is required based on how the closure uses captured variables
- [ ] Compare Rust closures with Java lambdas (effectively-final restriction, no mutable capture) and Go anonymous functions (capture by reference to variable, not value)

## Exercises
- [ ] **Closure basics**: Write closures that add, multiply, and greet by name; store each in a variable and call it. Annotate one with explicit types and let the others infer. Verify you cannot give a closure two different signatures.
- [ ] **Capture modes**: Create a `Vec<String>`, then write three closures: one that reads it (borrows `&`), one that pushes to it (borrows `&mut`), and one that moves it into the closure and drops it. Print the closure trait each requires (`Fn`, `FnMut`, `FnOnce`) by passing them to helper functions with those bounds.
- [ ] **Passing closures to functions**: Write a function `apply_twice<F: Fn(i32) -> i32>(f: F, x: i32) -> i32` that applies the closure twice. Test it with a closure that doubles its input and one that adds 10.
- [ ] **FnOnce in practice**: Write a closure that captures a `String` by value and returns it (consuming the captured value). Demonstrate that calling it a second time causes a compile error. Then write a function `consume_and_print<F: FnOnce() -> String>(f: F)` and pass the closure to it.

## Notes
_Lesson not yet started._
