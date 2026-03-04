# Lesson 069: Practical declarative macros - useful patterns, debugging macros

## Section 15: Macros

## Status: pending

## Added
- Initial curriculum design [NEW - bridging lesson]

## Objectives
- [ ] Write macros that reduce real-world boilerplate (enum variant constructors, repetitive `impl` blocks)
- [ ] Create a `hashmap!{}` macro for convenient `HashMap` initialization (similar to how `vec![]` works)
- [ ] Build macros that generate builder-pattern or constructor code for structs
- [ ] Debug macros using `cargo expand` and `trace_macros!(true)` to trace macro invocation at compile time
- [ ] Identify and avoid common macro pitfalls: unexpected token captures, eager vs lazy evaluation, type ambiguity

## Exercises
- [ ] **hashmap! macro**: Write a `hashmap!` macro that accepts `key => value` pairs and returns a `HashMap`; support both trailing comma and no trailing comma; test with `hashmap!{ "a" => 1, "b" => 2 }` and verify the contents
- [ ] **Impl block generator**: Write a `impl_display!` macro that takes a struct name and a format string, and generates an `impl std::fmt::Display` for that struct; test with at least 2 different structs
- [ ] **Struct constructor macro [STRETCH]**: Write a `new_struct!` macro that takes a struct name and field definitions, generates the struct definition AND a `new()` associated function that takes all fields as parameters; test by constructing instances with the generated `new()`
- [ ] **Debug a broken macro**: Start with a deliberately broken macro (provided as a comment with known bugs -- e.g., wrong fragment specifier, missing repetition separator); use `cargo expand` to diagnose the issue, fix the macro, and add comments explaining what was wrong

## Notes
_Lesson not yet started._
