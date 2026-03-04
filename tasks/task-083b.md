# Lesson 083b: Fuzzing with cargo-fuzz

## Section 18: Testing & Quality

## Status: pending

## Prerequisites
- Nightly Rust toolchain (`rustup install nightly`)
- Lesson 083a (property-based testing with proptest)

## Added
- Split from lesson 083 (v6 pacing review)

## Objectives
- [ ] Understand fuzzing vs property-based testing: fuzzing feeds random/mutated byte sequences to find crashes and panics, while property testing verifies logical invariants with structured data
- [ ] Set up `cargo-fuzz` with nightly Rust: install the tool, initialize a fuzz project, and understand the fuzz target structure
- [ ] Write fuzz targets and interpret results: create fuzz targets for parsing/deserialization functions, run the fuzzer, analyze crash reports, and add regression tests

## Exercises
- [ ] **Exercise 1 -- Fuzz a parser**: Write a simple `fn parse_key_value(input: &[u8]) -> Result<(String, String), ParseError>` that parses `key=value` from raw bytes. Set up `cargo-fuzz` with a fuzz target that feeds random bytes to this parser. Run the fuzzer for 1-2 minutes and document any panics or unexpected behaviors found.
- [ ] **Exercise 2 -- Fix and regress**: Fix the bugs found by fuzzing in Exercise 1. Add the crash inputs as regression tests (unit tests with the exact byte sequences that caused crashes). Re-run the fuzzer to verify the fixes hold.

## Notes
_Lesson not yet started._
_Split from original lesson 083 which covered both proptest and cargo-fuzz (~1.75-2.5 hr estimated). This part focuses on cargo-fuzz only._
_Requires nightly Rust: `rustup install nightly`. Run cargo-fuzz commands with `cargo +nightly fuzz`._
