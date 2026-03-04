# Lesson 096: Project 1 - continued (testing, publishing)

## Section 21: Capstone Projects

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Write comprehensive unit tests for all modules of the CLI tool: config parsing, text transformations, validation logic, and error formatting
- [ ] Write integration tests that invoke the binary end-to-end using `assert_cmd` and `predicates`, verifying correct output and exit codes for success and error cases
- [ ] Add documentation comments (`///`) with examples to all public functions and types, and verify examples compile with `cargo test` (doc tests)
- [ ] Set up a GitHub Actions CI workflow that runs `cargo check`, `cargo clippy`, `cargo fmt --check`, and `cargo test` on push
- [ ] Polish the CLI with a progress indicator for large files (using `indicatif`), colored error output (using `colored` or `anstream`), and a `--verbose` flag for debug information

## Exercises
- [ ] **Exercise 1 - Unit Tests for Config and Transformations**: Write unit tests for the config parsing and text transformation modules: test loading valid TOML config, missing required fields, invalid field values, and `#[serde(default)]` defaults -- test each transformation function (uppercase, keyword filter, line numbering, blank-line removal) with known input/output pairs -- use `tempfile` to create test config files or test from string literals
- [ ] **Exercise 2 - Integration Tests with assert_cmd**: Write integration tests using `assert_cmd`: test that `fileproc process --config test.toml input.txt` produces expected output, that `fileproc stats input.txt` prints correct line/word/char counts, that invalid arguments print usage help, that missing files produce a clear error message, and that `--help` works for all subcommands
- [ ] **Exercise 3 - Documentation and Doc Tests**: Add `///` doc comments to all public types and functions in the library portion of the crate, including at least two `# Examples` blocks that demonstrate usage -- run `cargo test` to verify doc examples compile and pass, then run `cargo doc --open` to review the generated documentation
- [ ] **Exercise 4 - CI Workflow for fileproc**: Create a `.github/workflows/ci.yml` file for the `fileproc` project: run the test suite on Ubuntu latest with stable Rust, cache the cargo registry and target directory, and add steps for clippy (with `-D warnings` to fail on warnings) and rustfmt checking. _Note: Lesson 085 teaches generic CI/CD concepts (matrix builds, cross-compilation, release workflows). This exercise is about applying those concepts to your specific `fileproc` project -- a single-target CI pipeline with project-specific test steps, not the full matrix/release setup from 085._
- [ ] **Exercise 5 - Dry-Run Publish**: Run `cargo publish --dry-run` to verify your crate is ready for publishing. Review the output for any warnings or errors. (Do NOT actually publish.)

## New Crates Introduced

These crates are used for the first time in this lesson. Brief introductions:

- **`assert_cmd`** -- Provides a fluent API for testing CLI binaries from integration tests. Lets you invoke your compiled binary, pass arguments, pipe stdin, and assert on stdout, stderr, and exit codes.
- **`predicates`** -- A companion to `assert_cmd` that provides composable boolean predicates for assertions (e.g., `predicate::str::contains("error")`, `predicate::str::is_empty()`). Used to write expressive test assertions on command output.
- **`tempfile`** -- Creates temporary files and directories that are automatically cleaned up when dropped. Useful in tests for creating throwaway config files or input data without polluting the filesystem.
- **`indicatif`** -- Provides progress bars, spinners, and multi-progress displays for CLI applications. Useful for showing processing progress on large files.
- **`colored`** -- Adds ANSI color and style formatting to terminal output (e.g., `"error".red().bold()`). Used to make error messages and status output more readable in the terminal.

## Notes
- **SUPERSEDED**: This lesson was split into task-096a.md (testing) and task-096b.md (documentation, CI, publishing) during v13 pacing review (2026-03-04). Use those files instead.
- _Lesson not yet started._
