# Lesson 096b: Project 1 Part D - Documentation, CI, and Publishing

## Section 21: Capstone Projects (split from lesson 096)

## Status: pending

## Added
- Split from task-096 (v13 pacing review, 2026-03-04)

## New Crates Introduced

- **`indicatif`** -- Provides progress bars, spinners, and multi-progress displays for CLI applications. Useful for showing processing progress on large files.
- **`colored`** -- Adds ANSI color and style formatting to terminal output (e.g., `"error".red().bold()`). Used to make error messages and status output more readable in the terminal.

## Objectives
- [ ] Add documentation comments (`///`) with examples to all public functions and types, and verify examples compile with `cargo test` (doc tests)
- [ ] Set up a GitHub Actions CI workflow that runs `cargo check`, `cargo clippy`, `cargo fmt --check`, and `cargo test` on push
- [ ] Polish the CLI with a progress indicator for large files (using `indicatif`), colored error output (using `colored` or `anstream`), and a `--verbose` flag for debug information

## Exercises
- [ ] **Exercise 1 - Documentation and Doc Tests**: Add `///` doc comments to all public types and functions in the library portion of the crate, including at least two `# Examples` blocks that demonstrate usage -- run `cargo test` to verify doc examples compile and pass, then run `cargo doc --open` to review the generated documentation
- [ ] **Exercise 2 - CI Workflow for fileproc**: Create a `.github/workflows/ci.yml` file for the `fileproc` project: run the test suite on Ubuntu latest with stable Rust, cache the cargo registry and target directory, and add steps for clippy (with `-D warnings` to fail on warnings) and rustfmt checking. _Note: Lesson 085 teaches generic CI/CD concepts (matrix builds, cross-compilation, release workflows). This exercise is about applying those concepts to your specific `fileproc` project._
- [ ] **Exercise 3 - Dry-Run Publish**: Run `cargo publish --dry-run` to verify your crate is ready for publishing. Review the output for any warnings or errors. (Do NOT actually publish.)
- [ ] **Exercise 4 [STRETCH] -- CLI polish**: Add a progress indicator using `indicatif` for large file processing and colored output using `colored` for success/error messages. These crates are introduced above.

## Notes
- ~1-1.5 hours estimated
- Prerequisite: 096a (testing the CLI tool)
