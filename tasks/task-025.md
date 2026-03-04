# Lesson 025: Pattern matching - match, if let, while let, destructuring

## Section 5: Structuring Data

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Use `match` expressions to handle every variant of an enum, understanding that match is exhaustive (the compiler enforces all cases are covered)
- [ ] Destructure enums, structs, and tuples within match arms to extract inner data (e.g., `Message::Move { x, y } => ...`)
- [ ] Use `if let` as syntactic sugar for matching a single pattern, and `while let` for looping while a pattern matches
- [ ] Use the `_` wildcard to ignore values and `..` to ignore remaining fields in structs or tuple positions
- [ ] Understand that match arms are expressions -- they return values, enabling `let result = match x { ... }`

## Exercises
- [ ] **Exercise 1 - Exhaustive enum matching**: Using the `Message` enum from lesson 024, write a `match` expression that handles every variant and returns a descriptive `String`. Try removing one arm and observe the compiler error. Add a `catch-all` arm with `_` and discuss when catch-alls are appropriate vs dangerous.
- [ ] **Exercise 2 - Struct destructuring in match**: Create a `Shape` enum with `Circle { radius: f64 }`, `Rectangle { width: f64, height: f64 }`, and `Triangle { base: f64, height: f64 }`. Write `fn area(shape: &Shape) -> f64` using match with destructuring. Then write `fn describe(shape: &Shape) -> String` that uses `..` to ignore some fields.
- [ ] **Exercise 3 - if let and while let**: Use `if let Some(value) = option_variable` to conditionally extract a value. Then try a simple `while let`: create a `Vec<i32>`, then use `while let Some(val) = vec.pop() { println!("{}", val); }` to drain it. Then try the nested pattern with `Vec<Option<i32>>`: use `while let Some(Some(val)) = vec.pop()` to process values until encountering a `None`. Compare `if let` with a full match -- when is each more readable?
- [ ] **Exercise 4 - Command parser**: Build a simple command parser: define a `Command` enum with `Ping`, `Echo(String)`, `Set { key: String, value: String }`, and `Unknown(String)`. Write `fn parse_command(input: &str) -> Command` that splits the input string and matches on the command word. Then write `fn execute(cmd: Command) -> String` using match to return the appropriate response. Use `let result = match ... { }` to demonstrate match as an expression.

## Notes
_Lesson not yet started._
