# Lesson 001: Installing Rust, toolchain overview (rustup, rustc, cargo)

## Section 1: Getting Started

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Install Rust via rustup and verify that `rustc --version`, `cargo --version`, and `rustup --version` all produce output
- [ ] Explain the role of each toolchain component: rustup (toolchain manager), rustc (compiler), and cargo (build system + package manager), and how they compare to Java's JDK/Maven/Gradle and Go's `go` tool
- [ ] Understand Rust editions (2015, 2018, 2021, 2024) and how they relate to backward compatibility — compare to Java's release model and Go's `go.mod` version directive
- [ ] Use `rustup show` to inspect the active toolchain and `rustup doc` to open local documentation
- [ ] Compile a standalone `.rs` file directly with `rustc` and run the resulting binary, understanding that cargo is the standard way but rustc works for single files

## Exercises
- [ ] **Exercise 1 — Install and verify**: Install Rust using `curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh`. Run `rustc --version`, `cargo --version`, and `rustup show`. Record the output in a comment at the top of your first source file.
- [ ] **Exercise 2 — Compile with rustc**: Create a file `hello.rs` containing a `main()` function that prints "Hello from rustc!". Compile it with `rustc hello.rs` and run `./hello`. Observe the binary size and compare it to a similar Go binary (`go build`) or Java class file.
- [ ] **Exercise 3 — Create your first cargo project**: Run `cargo new lesson-001 --name lesson_001` and explore the generated directory structure. Run `cargo run` inside the project and confirm "Hello, world!" prints. Read through the generated `Cargo.toml` and `src/main.rs` files.
- [ ] **Exercise 4 — Explore the toolchain**: Run `rustup doc --std` to open the standard library docs locally. Find the documentation page for `println!`. Run `rustup component list` and note which components are installed by default.

## Notes
_Lesson not yet started._
