# Lesson 030: Result<T,E>, the ? operator, propagation

## Section 7: Error Handling

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Understand the `Result<T, E>` enum and its two variants `Ok(T)` and `Err(E)`, and how it replaces exceptions
- [ ] Use `match` on `Result` to handle both success and error cases explicitly
- [ ] Use the `?` operator to propagate errors up the call stack, and understand that it calls `From::from()` on the error
- [ ] Chain `?` across multiple function calls to build pipelines of fallible operations
- [ ] Compare `Result` with Java's checked exceptions / try-catch and Go's `(val, err)` return pattern

## Exercises
- [ ] **Exercise 1 - File reading with Result**: Write a function `fn read_config(path: &str) -> Result<String, std::io::Error>` that reads a file and returns its contents. Handle both the file-exists and file-not-found cases in the caller using `match`
- [ ] **Exercise 2 - Propagate with ?**: Rewrite the function from Exercise 1 to use `?` instead of `match`. Then write a second function that calls it and also uses `?`, demonstrating two levels of propagation
- [ ] **Exercise 3 - Convert unwrap to Result**: Refactor this unwrap-heavy code to return `Result` and use `?`:
  ```rust
  // Refactor this code to use ? and Result:
  fn read_config() -> String {
      let contents = std::fs::read_to_string("config.toml").unwrap();
      let port: u16 = contents.lines()
          .find(|l| l.starts_with("port"))
          .unwrap()
          .split('=')
          .nth(1)
          .unwrap()
          .trim()
          .parse()
          .unwrap();
      format!("Port: {}", port)
  }
  ```
- [ ] **Exercise 4 - Multi-step pipeline**: Build a function `fn process_user_input(input: &str) -> Result<u32, String>` that: (1) trims whitespace, (2) parses to u32, (3) validates the number is in range 1..=100. Each step should produce a meaningful error message. Chain all three steps using `?` with `map_err()`. `map_err(|e| ...)` transforms the error type of a `Result` while leaving the `Ok` value unchanged -- useful when you need to convert between different error types during propagation

## Notes
_Lesson not yet started._
