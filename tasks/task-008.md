# Lesson 008: Functions, parameters, return values, expressions vs statements

## Section 2: Language Basics

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Define functions with typed parameters and return types using `fn name(param: Type) -> ReturnType` syntax (contrast with Go's `func` and Java's method signatures)
- [ ] Understand the critical difference between expressions (produce a value, no semicolon) and statements (perform an action, end with semicolon) - this is unlike Java/Go where everything is a statement
- [ ] Use implicit return (last expression without semicolon) and explicit `return` keyword, knowing when each is idiomatic
- [ ] Understand the unit type `()` as the default return when no return type is specified, and what happens when you accidentally add a semicolon to the last expression
- [ ] Know about diverging functions with the never type `!` (e.g., functions that always panic or loop forever)

## Exercises
- [ ] **Exercise 1 - Expression vs statement**: Write a function `add_one(x: i32) -> i32` using implicit return (no `return` keyword, no semicolon). Then accidentally add a semicolon and read the compiler error carefully. Fix it. Write another version using explicit `return` and compare
- [ ] **Exercise 2 - Block expressions**: Use a block `{}` as an expression to assign a value: `let result = { let a = 5; let b = 10; a + b };`. Extend this to a function that uses intermediate blocks for computation. Verify that blocks can be used anywhere an expression is expected
- [ ] **Exercise 3 - Mini calculator**: Write four functions (`add`, `subtract`, `multiply`, `divide`) that each take two `f64` parameters. The `divide` function should return `f64` but print a warning and return `0.0` if the divisor is zero (use early `return`). Write a `main` that exercises all four
- [ ] **Exercise 4 - Function composition**: Write a function `apply_twice(x: i32, f: fn(i32) -> i32) -> i32` that applies function `f` to `x` two times. Pass it a `double` function and a `square` function. This previews function pointers (closures come later in lesson 51)

## Notes
_Lesson not yet started._
