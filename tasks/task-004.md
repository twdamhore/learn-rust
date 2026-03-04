# Lesson 004: Hello World, println!, formatting, comments, basic I/O

## Section 1: Getting Started

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Understand the `fn main()` entry point — Rust requires an explicit `main` function (like Go and Java), but returns `()` by default (or `Result` for error handling later)
- [ ] Use `println!` and `eprintln!` macros with format strings: positional `{}`, named `{name}`, debug `{:?}`, pretty-debug `{:#?}`, and padding/alignment `{:>10}` — understand that `!` means it is a macro, not a function
- [ ] Know the three comment styles: line comments `//`, block comments `/* */`, and doc comments `///` (outer) and `//!` (inner) — understand that `///` generates documentation via `cargo doc`
- [ ] Read input from stdin using `std::io::stdin().read_line()` and handle the `Result` it returns with `.expect()` — compare to Go's `fmt.Scan` and Java's `Scanner`
- [ ] Parse string input to numeric types using `.trim().parse::<T>()` and handle the `Result` with `match` or `.expect()`

> **Preview**: The `Result` type and `match` patterns are explained fully in lessons 29-30. For now, just follow the patterns shown.

## Exercises
- [ ] **Exercise 1 — Format string showcase**: Write a program that demonstrates at least 6 different format specifiers in `println!`: `{}` (Display), `{:?}` (Debug), `{:#?}` (pretty Debug), `{:>20}` (right-aligned), `{:.2}` (2 decimal places for floats), and `{:08b}` (binary with zero-padding). Print a table of values showing each format applied to sample data.
- [ ] **Exercise 2 — Echo program with line numbers**: Write a program that reads lines from stdin in a loop. For each line, print it back prefixed with a line number (e.g., `1: hello`). Exit the loop when the user types "quit". Use `eprintln!` to print a final summary like "Read 5 lines total" to stderr.

  > **Starter template** for the echo loop:
  > ```rust
  > use std::io::{self, BufRead};
  >
  > fn main() {
  >     let stdin = io::stdin();
  >     let mut line_number = 1;
  >     for line in stdin.lock().lines() {
  >         let line = line.expect("Failed to read line");
  >         if line == "quit" {
  >             break;
  >         }
  >         println!("{}: {}", line_number, line);
  >         line_number += 1;
  >     }
  > }
  > ```
  > This uses `BufRead::lines()` which is simpler than the manual `loop`/`read_line` approach. `BufRead`, `lines()`, and `expect()` will be explained in later lessons -- for now, use this as a template and focus on the `println!` formatting.
- [ ] **Exercise 3 — Temperature converter**: Write a program that prompts the user to enter a temperature value and a unit (C or F). Read the input, parse the number, and convert Celsius to Fahrenheit or vice versa. Print the result formatted to 1 decimal place (e.g., `100.0°C = 212.0°F`). Handle invalid input with a helpful error message using `.expect()` or a `match` on the parse result.

  > **Hint** -- Reading and parsing input:
  > ```rust
  > let mut input = String::new();
  > std::io::stdin().read_line(&mut input).expect("Failed to read line");
  > let value: f64 = input.trim().parse().expect("Please enter a number");
  > ```
- [ ] **Exercise 4 — Self-documenting code** [OPTIONAL]: Write a small library file (`src/lib.rs`) with at least 2 public functions that include `///` doc comments with `# Examples` sections. Run `cargo doc --open` to generate and view the HTML documentation. Add a `//!` module-level doc comment at the top of the file describing what the module does.

## Notes
_Lesson not yet started._
