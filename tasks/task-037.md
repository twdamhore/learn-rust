# Lesson 037: String in depth - UTF-8, indexing, manipulation

## Section 8: Collections & Iterators

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Understand `String`'s internal structure as a `Vec<u8>` wrapper that guarantees valid UTF-8
- [ ] Work with UTF-8 encoding: understand why indexing by byte position can panic on multi-byte characters, and why `String` does not implement `Index<usize>`
- [ ] Iterate over a `String` by `.chars()` (Unicode scalar values) vs `.bytes()` (raw bytes) and understand when to use each
- [ ] Safely slice strings using byte ranges while ensuring you don't split a multi-byte character (and what happens if you do)
- [ ] Use common string methods: `contains`, `replace`, `split`, `trim`, `starts_with`, `to_uppercase`, and `format!` macro for building strings

## Exercises
- [ ] **Exercise 1 - Chars vs bytes**: Create a string containing English, emoji, and CJK characters (e.g., `"Hello world"`). Print its `.len()` (byte count) and `.chars().count()` (character count). Iterate with `.chars()` and `.bytes()` and print each, observing how multi-byte characters appear
- [ ] **Exercise 2 - Safe slicing**: Write a function `fn safe_substring(s: &str, start: usize, end: usize) -> Option<&str>` that returns a slice only if both `start` and `end` fall on character boundaries (use `.is_char_boundary()`). Test with ASCII strings and multi-byte strings
- [ ] **Exercise 3 - String building**: Concatenate strings three ways: (1) using `+` operator (note it takes ownership of the left side), (2) using `format!()`, (3) using `String::new()` + `push_str()`. Build the same sentence with each approach and discuss which is clearest and most efficient
- [ ] **Exercise 4 - CSV line parser**: Write `fn parse_csv_line(line: &str) -> Vec<&str>` that splits a line by commas, trims whitespace from each field, and returns the fields. Handle edge cases: empty fields, trailing commas, leading/trailing whitespace. Write tests for each case
  > **Hint**: If you encounter lifetime errors when returning `&str` slices from parsed lines, remember that the slice borrows from the input string. Consider whether your function should return owned `String` values or require the caller to keep the source string alive.

## Notes
_Lesson not yet started._
