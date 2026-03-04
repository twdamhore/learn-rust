# Lesson 005: Variables, mutability, constants, shadowing

## Section 2: Language Basics

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Understand `let` bindings and why variables are immutable by default in Rust (contrast with Java's `final` being opt-in and Go's `:=` reassignment)
- [ ] Use the `mut` keyword to make variables mutable, and understand when mutability is appropriate
- [ ] Distinguish between `const` and `let` - compile-time vs runtime, naming conventions (`SCREAMING_SNAKE_CASE`), type annotation requirement, and global scope
- [ ] Use shadowing to rebind a variable name (including changing its type), and understand how this differs from mutability
- [ ] Read and interpret compiler error messages related to immutability and unused variables

## Exercises
- [ ] **Exercise 1 - Mutability explorer**: Declare an immutable variable, attempt to reassign it (observe the compiler error), then fix it with `mut`. Declare a mutable variable and mutate it several times, printing the value after each change
- [ ] **Exercise 2 - Shadowing type change**: Create a `let` binding with a string value `"42"`, then shadow it by parsing it into an integer. Print both the string and integer versions (using separate scopes or sequential shadowing). Try the same with `mut` and observe why it fails (type mismatch)
- [ ] **Exercise 3 - Constants vs let**: Define a `const MAX_SCORE: u32 = 100;` and a `let` binding. Try to use `mut` with `const` (observe the error). Try to assign a runtime value (e.g., a function call) to a `const` (observe the error). Summarize the differences in a comment
- [ ] **Exercise 4 - Predict the output**: Write a program with nested scopes and shadowing, then predict what each `println!` will output before running it. Example: shadow a variable in an inner block, then print it after the block ends to see the outer value restored

## Notes
_Lesson not yet started._
