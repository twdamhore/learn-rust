# Lesson 034: Error ecosystem - thiserror, anyhow, best practices

## Section 7: Error Handling

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Use `thiserror` to derive `Display` and `Error` implementations automatically with `#[error("...")]` and `#[from]` attributes
- [ ] Use `anyhow::Result` and `anyhow::Error` for application-level error handling where you don't need to match on specific error types
- [ ] Understand when to use `thiserror` (library crates exposing typed errors) vs `anyhow` (application code, scripts, CLIs)
- [ ] Use `anyhow::Context` and `.context("message")` to add human-readable context to errors as they propagate
- [ ] Downcast `anyhow::Error` back to a concrete type with `.downcast_ref::<T>()` when needed

## Exercises
- [ ] **Exercise 1 - Rewrite with thiserror**: Take the manual `AppError` from lesson 033 and rewrite it using `thiserror`. Use `#[error("...")]` for Display messages and `#[from]` for automatic From implementations. Verify the behavior is identical
- [ ] **Exercise 2 - CLI app with anyhow**: Build a small CLI tool that reads a filename from args, opens the file, parses each line as an integer, and sums them. Use `anyhow::Result<()>` for `main()` and `?` everywhere. Observe how different error types are unified
- [ ] **Exercise 3 - Adding context**: Enhance Exercise 2 to use `.with_context(|| format!("failed to read line {} of {}", line_num, filename))` so error messages include which file and line caused the failure
- [ ] **Exercise 4 - thiserror in a library, anyhow in a binary**: Create a small library module with `thiserror` errors and a binary that uses it through `anyhow`. Demonstrate converting from the library's typed error to `anyhow::Error`, then downcasting it back to the original type. Use `error.downcast_ref::<YourErrorType>()` to attempt the downcast. This returns `Option<&YourErrorType>`. Example: `if let Some(io_err) = err.downcast_ref::<std::io::Error>() { ... }`

## Notes
_Lesson not yet started._
