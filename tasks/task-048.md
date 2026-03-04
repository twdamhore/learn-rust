# Lesson 048: What lifetimes are, lifetime annotations 'a

## Section 10: Lifetimes

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Understand what lifetimes represent: every reference in Rust has a lifetime, which is the scope during which that reference is valid. Lifetimes are the compiler's tool for ensuring references never outlive the data they point to
- [ ] Read and write lifetime annotations (`'a`, `'b`, etc.) on function signatures, understanding that annotations do not change how long values live -- they describe relationships between the lifetimes of references
- [ ] Understand why the compiler needs lifetime hints: when a function takes multiple references and returns a reference, the compiler cannot always determine which input the return value borrows from without annotations
- [ ] Write the classic `longest()` function with lifetime annotations and trace through how the compiler uses the annotations to validate calling code
- [ ] Understand dangling reference prevention: Rust will not compile code where a reference could outlive the data it refers to, and compare this with Java (no dangling references due to GC) and Go (GC + escape analysis)

## Exercises
- [ ] **Trigger the error**: Write a function `fn first_word(s: &str) -> &str` that returns a substring -- it compiles fine (elision). Then write `fn pick(a: &str, b: &str) -> &str` that returns one of its arguments -- observe the "missing lifetime specifier" error and understand why elision cannot help here
- [ ] **Annotate longest()**: Implement `fn longest<'a>(x: &'a str, y: &'a str) -> &'a str` that returns the longer string. Write test cases including one where `x` and `y` have different scopes, and verify the returned reference is only valid for the shorter of the two lifetimes
- [ ] **Lifetime scope tracing**: Given this code pattern, predict whether it compiles and explain why: `let result; { let s = String::from("hello"); result = &s; } println!("{}", result);` -- then try variations where the string outlives the reference and verify your predictions
- [ ] **Single-input lifetime**: Write `fn first_sentence(text: &str) -> &str` that returns everything up to the first period. Observe that this compiles without annotations (elision rule 1). Then write the explicitly annotated version and confirm both are equivalent

## Notes
_Lesson not yet started._
