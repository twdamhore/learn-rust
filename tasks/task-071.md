# Lesson 071: Procedural macros - function-like, derive macros

## Section 15: Macros

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Understand the three types of procedural macros: function-like, derive, and attribute macros
- [ ] Set up a proc macro crate with `proc-macro = true` in `Cargo.toml` and understand why proc macros must live in their own crate
- [ ] Use `syn` to parse Rust code into an AST (`DeriveInput`, `ItemFn`, etc.) and `quote` to generate `TokenStream` output
- [ ] Write a basic derive macro that auto-implements a trait for structs
- [ ] Understand `TokenStream` as the input/output currency of proc macros and how `proc_macro2` bridges compile-time and test-time

## Exercises
- [ ] **Derive macro - Hello trait**: Create a proc macro crate; define a `Hello` trait with a `fn hello() -> String` method; write a `#[derive(Hello)]` macro that implements it by returning `"Hello, I am <StructName>!"`; test with multiple structs
- [ ] **Function-like proc macro**: Write a function-like proc macro `make_getter!` that takes a struct definition as input and generates getter methods for each field; e.g., a struct with `name: String` gets a `fn name(&self) -> &str` method
- [ ] **Parse struct fields**: Write a derive macro `FieldNames` that implements a trait method `fn field_names() -> Vec<&'static str>` returning the names of all fields; use `syn::DeriveInput` and iterate over `fields` in `syn::Data::Struct`
- [ ] **Quote templating**: Explore `quote!` by writing a derive macro `Builder` that generates a builder struct with setter methods for each field; the builder has a `build()` method that returns the original struct; test with a struct having 3+ fields

## Notes
_**SUPERSEDED**: This lesson has been split into [Lesson 71a](task-071a.md) and [Lesson 71b](task-071b.md). Use those files instead._

_Lesson not yet started._
