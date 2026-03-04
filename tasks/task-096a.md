# Lesson 096a: Project 1 Part C - Testing the CLI Tool

## Section 21: Capstone Projects (split from lesson 096)

## Status: pending

## Added
- Split from task-096 (v13 pacing review, 2026-03-04)

## New Crates Introduced

These crates are used for the first time in this lesson. Brief introductions:

- **`assert_cmd`** -- Provides a fluent API for testing CLI binaries from integration tests. Lets you invoke your compiled binary, pass arguments, pipe stdin, and assert on stdout, stderr, and exit codes.
- **`predicates`** -- A companion to `assert_cmd` that provides composable boolean predicates for assertions (e.g., `predicate::str::contains("error")`, `predicate::str::is_empty()`). Used to write expressive test assertions on command output.
- **`tempfile`** -- Creates temporary files and directories that are automatically cleaned up when dropped. Useful in tests for creating throwaway config files or input data without polluting the filesystem.

## Objectives
- [ ] Write comprehensive unit tests for all modules of the CLI tool: config parsing, text transformations, validation logic, and error formatting
- [ ] Write integration tests that invoke the binary end-to-end using `assert_cmd` and `predicates`, verifying correct output and exit codes for success and error cases

## Exercises
- [ ] **Exercise 1 - Unit Tests for Config and Transformations**: Write unit tests for the config parsing and text transformation modules: test loading valid TOML config, missing required fields, invalid field values, and `#[serde(default)]` defaults -- test each transformation function (uppercase, keyword filter, line numbering, blank-line removal) with known input/output pairs -- use `tempfile` to create test config files or test from string literals
- [ ] **Exercise 2 - Integration Tests with assert_cmd**: Write integration tests using `assert_cmd`: test that `fileproc process --config test.toml input.txt` produces expected output, that `fileproc stats input.txt` prints correct line/word/char counts, that invalid arguments print usage help, that missing files produce a clear error message, and that `--help` works for all subcommands

## Notes
- ~1-1.5 hours estimated
- Continues in 096b (documentation, CI, publishing)
