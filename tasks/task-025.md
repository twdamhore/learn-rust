# Lesson 025: Modules - mod, file structure, visibility (pub)

## Section 6: Project Organization

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Declare inline modules with `mod name { ... }` and understand the module tree starting from the crate root (`main.rs` or `lib.rs`)
- [ ] Organize modules into files using both the `mod.rs` convention (`foo/mod.rs`) and the newer file-based convention (`foo.rs` + `foo/` directory), knowing both are valid
- [ ] Control visibility with `pub`, `pub(crate)`, `pub(super)`, and `pub(in path)`, understanding that everything is private by default in Rust (unlike Go's capitalization rule)
- [ ] Navigate the module tree using `crate::`, `super::`, and `self::` path prefixes
- [ ] Understand that structs have per-field visibility -- struct fields are private by default even if the struct is `pub`, unlike Go where the struct and field visibility are independent

## Exercises
- [ ] **Exercise 1 - Inline to file modules**: Start with a single `main.rs` containing two inline modules `mod math { pub fn add(...) }` and `mod strings { pub fn capitalize(...) }`. Refactor each module into its own file (`src/math.rs`, `src/strings.rs`) and verify everything compiles identically. Compare this with Go's package-per-directory model and Java's class-per-file convention.
- [ ] **Exercise 2 - Nested module hierarchy**: Create a library crate with the structure: `src/lib.rs` declares `mod shapes;`, `src/shapes/mod.rs` declares `pub mod circle;` and `pub mod rectangle;`, each sub-module defines a struct and methods. Use `crate::shapes::circle::Circle` from `lib.rs`. Practice both `super::` and `crate::` paths to reference items across the hierarchy.
- [ ] **Exercise 3 - Visibility controls**: In the shapes library, make `Circle`'s `radius` field private and provide a `pub fn new(radius: f64) -> Circle` constructor and a `pub fn radius(&self) -> f64` getter. Make a helper function `pub(crate)` so it is available within the crate but not to external users. Try accessing private fields from outside the module and observe the compiler error. Use `pub(super)` for a utility function only the parent module should see.
- [ ] **Exercise 4 - Module organization project**: Create a small `calculator` project with modules: `operations` (with sub-modules `arithmetic` and `comparison`), `input` (parsing user input), and `display` (formatting output). Wire them together in `main.rs`. Practice the pattern of re-exporting key items from parent modules (e.g., `pub use arithmetic::add;` in `operations/mod.rs`) to create a clean public API. (preview of lesson 26 — re-exports are covered there in detail)

## Skeleton Directory Structures

> **Exercise 2** directory layout (create before coding):
> ```
> src/
>   lib.rs          (declares mod shapes;)
>   shapes/
>     mod.rs        (declares pub mod circle; pub mod rectangle;)
>     circle.rs
>     rectangle.rs
> ```

> **Exercise 4** directory layout (create before coding):
> ```
> src/
>   main.rs         (uses all modules)
>   operations/
>     mod.rs        (declares pub mod arithmetic; pub mod comparison;)
>     arithmetic.rs
>     comparison.rs
>   input.rs
>   display.rs
> ```

## Notes
_Lesson not yet started._
