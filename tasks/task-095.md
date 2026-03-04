# Lesson 095: Project 1 - CLI tool (file processor with clap, serde, error handling)

## Section 21: Capstone Projects

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Design the architecture of a CLI file processing tool: decide on input format (CSV, JSON, or TOML), processing operations (filter, transform, aggregate), and output format (table, JSON, or CSV)
- [ ] Implement command-line argument parsing with `clap` derive API: subcommands (e.g., `process`, `validate`, `stats`), required and optional flags, file path arguments, and help text
- [ ] Implement configuration file loading with `serde`: deserialize a TOML or JSON config file into typed Rust structs, with defaults for optional fields using `#[serde(default)]`
- [ ] Implement file reading and data processing: read input files, apply transformations based on config/flags, and produce structured output
- [ ] Implement comprehensive error handling with `thiserror` for library errors and `anyhow` for application-level errors, providing user-friendly error messages with context

## Exercises
- [ ] Build `fileproc`, a CLI tool that reads a CSV file and applies operations based on a TOML config file -- the config specifies which columns to select, filter conditions (e.g., "age > 30"), and sort order; use `clap` for CLI: `fileproc process --config config.toml input.csv`
- [ ] Implement the `validate` subcommand that checks whether an input CSV matches an expected schema (column names and types) defined in the config file -- report all validation errors at once rather than stopping at the first one
- [ ] Implement the `stats` subcommand that computes summary statistics for numeric columns (count, min, max, mean, sum) and prints them in a formatted table using simple `println!`-based alignment or the `comfy-table` crate
- [ ] Add proper error handling throughout: use `thiserror` to define error enums for config parsing, file I/O, CSV parsing, and validation errors; use `anyhow` with `.context()` in `main` to wrap errors with user-friendly messages; ensure the tool prints helpful messages (not raw stack traces) and exits with appropriate codes

## Notes
_**SUPERSEDED**: This lesson has been split into [Lesson 95a](task-095a.md) and [Lesson 95b](task-095b.md). Use those files instead._

_Lesson not yet started._
