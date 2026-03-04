# Lesson 108: CLI Tool Setup and Core Processing

## Section 21: Capstone Projects

## Status: pending

## Prerequisites
- Lesson 097 (serde - for TOML config loading)
- Lesson 099 (clap - for CLI argument parsing)
- Lesson 034 (thiserror/anyhow - for error handling)

## Added
- Split from lesson 108 (v6 pacing review)

## Objectives
- [ ] Set up a CLI project with `clap` derive API and `serde` for configuration: create a new cargo project with the necessary dependencies
- [ ] Implement configuration file loading with `serde`: deserialize a TOML config file into typed Rust structs, with defaults for optional fields using `#[serde(default)]`
- [ ] Implement basic file reading and text processing: read input files line by line, collect basic statistics
- [ ] Add structured error handling with `thiserror` for library errors and `anyhow` for application-level errors

## Exercises
- [ ] **Exercise 1 -- Project setup with clap**: Create a `fileproc` project. Use `clap` derive API to define the CLI with 2 subcommands: `process` (takes an input file path and optional `--config` flag) and `stats` (takes an input file path). Add `--verbose` flag at the top level. Verify with `--help`.
- [ ] **Exercise 2 -- Config loading with serde**: Define a `Config` struct with fields for output format (text/json), transformations to apply (list of strings), and optional settings. Implement TOML config loading with `serde`. Use `#[serde(default)]` for optional fields. Handle missing config file gracefully.
- [ ] **Exercise 3 -- Stats subcommand and error handling**: Implement the `stats` subcommand: read a text file and report line count, word count, character count, and average line length. Define error types with `thiserror` (FileError, ConfigError). Use `anyhow` with `.context()` in main for user-friendly error messages.

## Notes
_Lesson not yet started._
_Split from original lesson 108 which was rated OVERLOADED (~2.5-3.5 hr). Simplified from original: removed expression-evaluator filter condition ("age > 30"), csv crate usage is optional (can work with plain text files)._
