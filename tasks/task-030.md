# Lesson 030: Publishing crates, documentation (///), cargo doc

## Section 6: Project Organization

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Write outer doc comments (`///`) for functions, structs, enums, and methods, and inner doc comments (`//!`) for modules and crate-level documentation
- [ ] Use `cargo doc --open` to generate and browse HTML documentation, understanding how it renders Markdown formatting, links, and code blocks
- [ ] Write code examples in doc comments using triple-backtick blocks that `cargo test` runs as doc tests, ensuring examples stay correct as code evolves
- [ ] Understand the crates.io publishing workflow: `cargo login`, `cargo package` (inspect what gets included), `cargo publish`, and semantic versioning requirements
- [ ] Use common doc comment sections (`# Examples`, `# Panics`, `# Errors`, `# Safety`) following Rust API documentation conventions

## Exercises
- [ ] **Exercise 1 - Document a library**: Take the `core` library from lesson 029 (or create a small library with 2-3 public structs and functions). Add `//!` crate-level docs at the top of `lib.rs` explaining the library's purpose. Add `///` doc comments to every public item with descriptions, parameter explanations, and return value descriptions. Run `cargo doc --open` and browse the generated documentation.
- [ ] **Exercise 2 - Doc tests**: Add `# Examples` sections to at least three doc comments with runnable code blocks. Ensure each example compiles and passes when running `cargo test`. Include one example that demonstrates error handling by using `# fn main() -> Result<(), Box<dyn std::error::Error>> {` hidden setup. (This `Box<dyn std::error::Error>` syntax will be explained in later lessons -- for now, treat it as boilerplate that lets your doc test use the `?` operator.) Intentionally break an example and observe how `cargo test` catches it.
- [ ] **Exercise 3 - Advanced doc features**: Use `[`link syntax`]` in doc comments to cross-reference other items in the crate (e.g., `/// See [`OtherStruct`] for more details`). Add `# Panics` and `# Errors` sections where appropriate. Use `#` prefix in code examples to hide boilerplate lines. Generate docs with `cargo doc --document-private-items` and compare with the default output.
- [ ] **Exercise 4 - Publish preparation**: Run `cargo package --list` to see what files would be included in a published crate. Ensure `Cargo.toml` has all required fields: `name`, `version`, `edition`, `description`, `license`, `repository`. Add a `README.md` that `cargo doc` will use as the crate landing page. Run `cargo package` to create the `.crate` file and inspect its contents. Do NOT actually publish -- just verify everything is ready. Compare this workflow with publishing a Java artifact to Maven Central or a Go module.

## Notes
_Lesson not yet started._
