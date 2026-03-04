# Lesson 003: Clippy, rustfmt, rust-analyzer - setting up your dev workflow

## Section 1: Getting Started

## Status: pending

## Added
- Initial curriculum design [NEW - bridging lesson]

## Objectives
- [ ] Run `cargo clippy` and understand its role as a linter — know the difference between clippy warnings and compiler warnings, and how clippy compares to Go's `go vet`/`staticcheck` or Java's SpotBugs/Error Prone
- [ ] Understand clippy lint levels (`warn`, `deny`, `allow`) and how to configure them via attributes (`#[allow(clippy::...)]`, `#[warn(clippy::...)]`) and via `Cargo.toml` or `.clippy.toml`
- [ ] Set up `rustfmt` for automatic code formatting — create a `rustfmt.toml` with custom settings (e.g., `max_width`, `edition`) and run `cargo fmt`. Compare to `gofmt` (Go) and Spotless/google-java-format (Java).
- [ ] Configure rust-analyzer in your editor (VS Code, IntelliJ, or Neovim) and verify that inline type hints, auto-completion, go-to-definition, and error highlighting all work
- [ ] Understand the Rust developer feedback loop: write code, see rust-analyzer errors inline, run `cargo check` for fast validation, run `cargo clippy` for deeper lints, and `cargo fmt` before committing

## Exercises
- [ ] **Exercise 1 — Clippy catches problems**: Start with this intentionally poor code:

  ```rust
  // Save this as src/main.rs and run `cargo clippy`
  fn main() {
      let x = 3.14;
      if x == 3.14 {
          println!("pi");
      }

      let mut scores = vec![1, 2, 3, 4, 5];
      for i in 0..scores.len() {
          println!("{}", scores[i]);
      }

      let s = "hello".to_string();
      let r = &s;
      if r.len() > 0 {
          println!("{}", r);
      }

      let _y: u32 = 10 as u32;
  }
  ```

  Run `cargo clippy` and fix each warning. You should see at least 4 issues: float comparison, manual indexing with `0..len`, `.len() > 0` instead of `!.is_empty()`, and a redundant `as` cast.
- [ ] **Exercise 2 — Configure rustfmt**: Create a `rustfmt.toml` in your project root with at least 3 custom settings (e.g., `max_width = 100`, `tab_spaces = 4`, `use_small_heuristics = "Max"`). Intentionally write badly formatted code (inconsistent indentation, long lines, awkward brace placement). Run `cargo fmt` and observe the changes. Run `cargo fmt -- --check` to verify no formatting issues remain.
- [ ] **Exercise 3 — Lint levels**: Write a small program that triggers a clippy warning. First suppress it with `#[allow(clippy::...)]` and verify clippy passes. Then change it to `#[deny(clippy::...)]` and confirm it now produces an error instead of a warning. Finally, add a project-wide lint setting in your `main.rs` using `#![warn(clippy::pedantic)]` and observe the additional lints it catches.

  > **Hint**: Try writing code like `if vec.len() > 0 { ... }` (clippy suggests `!vec.is_empty()`), or `let x = 3.14;` without specifying the type (clippy may suggest `3.14_f64`), or using `&String` as a function parameter instead of `&str`.
- [ ] **Exercise 4 — IDE verification**: Open your project in your editor with rust-analyzer enabled. Verify the following work: (1) hover over a variable to see its inferred type, (2) trigger an error (e.g., type mismatch) and see the inline diagnostic, (3) use go-to-definition on `println!`, (4) use auto-complete to discover methods on a `String`. Take note of any settings you customized for your editor.

## Notes
_Lesson not yet started._
