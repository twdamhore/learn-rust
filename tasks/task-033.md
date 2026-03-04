# Lesson 033: Custom error types, From trait, error conversion

## Section 7: Error Handling

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Define custom error enums with multiple variants, including variants that carry data (e.g., `InvalidInput(String)`, `IoError(std::io::Error)`)
- [ ] Implement `std::fmt::Display` for custom error types to produce human-readable error messages
- [ ] Implement `std::error::Error` for custom error types, including the `source()` method for error chaining. The return type `Option<&(dyn Error + 'static)>` means 'an optional reference to any error type.' The `dyn Error` and `'static` syntax will be fully explained in later lessons (043 and 046) -- for now, follow the pattern.
- [ ] Implement `From<OtherError>` for your custom error to enable automatic conversion with `?`
- [ ] Design an error hierarchy for a small application, deciding which errors wrap others

---

### Prerequisite: Implementing a Trait

This lesson requires implementing traits for your types. Here's the template:

```rust
use std::fmt;

// Define a trait (or use one from std)
trait MyTrait {
    fn my_method(&self) -> String;
}

// Implement it for your type
struct MyType { /* fields */ }

impl MyTrait for MyType {
    fn my_method(&self) -> String {
        // implementation
        String::from("hello")
    }
}

// Example: implementing Display (from std::fmt)
impl fmt::Display for MyType {
    fn fmt(&self, f: &mut fmt::Formatter<'_>) -> fmt::Result {
        write!(f, "MyType")
    }
}
```

---

## Exercises
- [ ] **Exercise 1 - Custom error enum**: Create an `AppError` enum with variants `NotFound { item: String }`, `ParseFailure(std::num::ParseIntError)`, and `InvalidConfig(String)`. Implement `Display` to give each variant a readable message
- [ ] **Exercise 2 - Error trait implementation**: Implement `std::error::Error` for `AppError`. For the `ParseFailure` variant, return the inner error from `source()`. Verify error chaining works by printing the source
- [ ] **Exercise 3 - From trait for conversion**: Implement `From<std::io::Error>` and `From<std::num::ParseIntError>` for `AppError`. Write a function that reads a file and parses its first line as an integer, using `?` to automatically convert both error types
- [ ] **Exercise 4 [STRETCH] - Config parser errors**: Build an error type `ConfigError` for a simple key=value config file parser. It should handle: missing file, malformed line (no `=`), missing required key, and invalid value type. Write the parser and demonstrate each error case

## Notes
_Lesson not yet started._
