# Lesson 071a: Procedural Macros - Part A: Setup and Derive Macros

## Section 15: Macros

## Status: pending

## Added
- Split from lesson 071 (v6 pacing review)

## Objectives
- [ ] Understand proc macro vs declarative macro -- when to use which, and the tradeoffs
- [ ] Set up a proc macro crate (`Cargo.toml` with `proc-macro = true`, `proc_macro2`/`quote`/`syn` dependencies)
- [ ] Write a simple derive macro (`HelloMacro`) that adds a method to any struct
- [ ] Understand `TokenStream` as input/output and how `proc_macro2` bridges compile-time and test-time

## Proc macro crate setup checklist

Follow these steps exactly before starting the exercises:

1. Create a workspace: `mkdir lesson-071 && cd lesson-071 && cargo init --name usage`
2. Create the proc macro crate: `cargo new my_macros --lib`
3. Edit `my_macros/Cargo.toml` -- add under `[lib]`: `proc-macro = true`
4. Add dependencies to `my_macros/Cargo.toml`:
   ```toml
   [dependencies]
   syn = { version = "2", features = ["full"] }
   quote = "1"
   proc-macro2 = "1"
   ```
5. Create workspace `Cargo.toml` in the root:
   ```toml
   [workspace]
   members = ["my_macros", "."]
   ```
6. Add `my_macros` as dependency in the root `Cargo.toml`:
   ```toml
   [dependencies]
   my_macros = { path = "my_macros" }
   ```
7. Verify: `cargo check` should compile both crates

## Exercises
- [ ] **Derive HelloMacro**: Create a proc macro crate and implement `#[derive(HelloMacro)]` that adds a `hello()` method printing the type name; use `syn::DeriveInput` to extract the struct name and `quote!` to generate the impl; test with multiple structs
- [ ] **Derive FieldNames**: Implement `#[derive(FieldNames)]` that adds a `field_names() -> Vec<&'static str>` method returning the names of all fields; iterate over `fields` in `syn::Data::Struct`; test with structs having different numbers of fields

## Notes
_Lesson not yet started._
