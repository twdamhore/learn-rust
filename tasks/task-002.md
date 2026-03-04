# Lesson 002: Cargo deep dive - new, build, run, check, project structure

## Section 1: Getting Started

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Understand the full `Cargo.toml` manifest structure: `[package]` (name, version, edition), `[dependencies]`, `[dev-dependencies]`, and `[profile.*]` sections
- [ ] Know the standard cargo project layout: `src/main.rs` (binary crate root), `src/lib.rs` (library crate root), `src/bin/` (extra binaries), `tests/`, `examples/`, `benches/`
- [ ] Use core cargo commands fluently: `cargo new`, `cargo init`, `cargo build`, `cargo run`, `cargo check`, `cargo clean`, and explain when to use `check` vs `build` (speed vs full compilation)
- [ ] Add an external crate dependency from crates.io, understand semantic versioning in Cargo, and inspect the generated `Cargo.lock` file
- [ ] Understand build profiles: `dev` (debug, unoptimized) vs `release` (optimized), how to use `cargo build --release`, and why debug builds are faster to compile but slower to run

## Exercises
- [ ] **Exercise 1 — Binary vs library crate**: Create a binary project with `cargo new hello-bin` and a library project with `cargo new hello-lib --lib`. Compare the generated file structures. In the library, write a public function `pub fn greet(name: &str) -> String` that returns a greeting. Verify it compiles with `cargo check`.
- [ ] **Exercise 2 — Add a dependency**: In `hello-bin`, add the `rand` crate as a dependency by editing `Cargo.toml` (e.g., `rand = "0.8"`). Write code in `main.rs` that generates and prints a random number between 1 and 100. Run `cargo build` and examine the `Cargo.lock` file to see the full dependency tree. Compare this to adding a dependency in Go (`go get`) or Java (Maven `pom.xml`).
- [ ] **Exercise 3 — Check vs build timing**: In your project, run `cargo clean`, then time `cargo check` with `time cargo check`. Run `cargo clean` again and time `cargo build`. Compare the two durations and note the difference. Then run `cargo build --release` and compare the binary sizes in `target/debug/` vs `target/release/`.
- [ ] **Exercise 4 — Explore target directory**: After building, explore the `target/` directory structure. Find the compiled binary in `target/debug/`. Run `cargo clean` and observe what gets removed. Create a second binary by adding a file `src/bin/extra.rs` with its own `fn main()` and run it with `cargo run --bin extra`.

## Notes
_Lesson not yet started._
