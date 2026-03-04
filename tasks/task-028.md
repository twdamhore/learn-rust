# Lesson 028: Crates, packages, use, re-exports, prelude pattern

## Section 6: Project Organization

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Understand the distinction between a crate (compilation unit -- either a binary or library), a package (one or more crates with a `Cargo.toml`), and a module (namespace within a crate)
- [ ] Use `use` declarations to bring paths into scope with various styles: `use std::collections::HashMap`, `use std::io::{self, Read, Write}`, and glob imports `use std::collections::*`
- [ ] Distinguish absolute paths (`crate::module::item`) from relative paths (`self::item`, `super::item`) and know when each is appropriate
- [ ] Create re-exports with `pub use` to present a clean public API that hides internal module structure, similar to Go's single-package-level namespace
- [ ] Understand the prelude concept -- what `std::prelude` auto-imports and how libraries define their own preludes

## Exercises
- [ ] **Exercise 1 - Use statement styles**: In a single program, practice all `use` styles: import a single item (`use std::collections::HashMap`), a nested group (`use std::io::{self, BufRead, Write}`), an alias (`use std::collections::HashMap as Map`), and a glob (`use std::fmt::*` -- then discuss why glob imports are discouraged in production code). Write code that exercises each imported item.
- [ ] **Exercise 2 - Re-exports for clean API**: Create a library with internal modules `internal::parser` and `internal::formatter`. In `lib.rs`, use `pub use internal::parser::parse;` and `pub use internal::formatter::format_output;` so users of the crate only need `use mycrate::{parse, format_output}` rather than knowing the internal structure. Write a binary crate that depends on this library and uses the re-exported API. To make a binary crate depend on a local library, add a path dependency to Cargo.toml: `mylib = { path = "../mylib" }`. Workspace setup (an alternative approach) is covered in lesson 029.
- [ ] **Exercise 3 - External crates**: Add the `rand` crate to `Cargo.toml` dependencies. Use `use rand::Rng;` to bring the trait into scope and generate random numbers. Add the `chrono` crate and use nested imports. Practice the workflow: find a crate on crates.io, add it to `Cargo.toml`, import with `use`, and call its API. Add these to your `[dependencies]`: `rand = "0.8"` and `chrono = "0.4"`. Compare this with Go's `go get` and Java's Maven/Gradle dependency model.
- [ ] **Exercise 4 - Exploring the prelude**: Write a program that uses `Vec`, `String`, `Option`, `Result`, and `println!` without any `use` statements. Then write the explicit paths for the types to understand where they live (e.g., `std::vec::Vec`, `std::string::String`). Note: `#[derive(Debug, Clone)]` is built into the language syntax (not imported from the prelude). Create a custom prelude module in a library crate: `pub mod prelude { pub use crate::MyType; pub use crate::MyTrait; }` and use it from a binary crate.

## Notes
_Lesson not yet started._
