# Lesson 018a: Strings Part A - String vs &str, When to Use Which

## Section 4: Strings & Slices (split from lesson 018)

## Status: pending

## Added
- Split from task-018 (v13 pacing review, 2026-03-04)

## Objectives
- [ ] Understand `String` vs `&str` thoroughly: `String` is an owned, growable, heap-allocated UTF-8 string; `&str` is a borrowed, immutable view into UTF-8 bytes (either heap-allocated String data, static binary data, or a slice of either)
- [ ] Know when to use each in function signatures: accept `&str` for read-only access (most common), accept `String` when the function needs to own/store the data, return `String` when creating new string data, return `&str` when returning a slice of input
- [ ] Convert fluently between `String` and `&str`: `&str` to `String` via `.to_string()`, `.to_owned()`, `String::from()`, or `.into()`; `String` to `&str` via `&s`, `&s[..]`, or `.as_str()`

## Exercises
- [ ] **Function signature practice**: Write these functions with the most idiomatic signature: (1) `is_palindrome` - checks if a string reads the same forwards and backwards, (2) `make_uppercase` - returns a new uppercase string, (3) `greet` - takes a name and returns "Hello, {name}!", (4) `add_greeting` - takes a mutable `Vec<String>` and a name, pushes "Hello, {name}!" into the Vec (shows when a function needs to own a `String`). For each, explain in comments why you chose `&str` vs `String` for the parameter and return type
- [ ] **String processing pipeline**: Build a function that takes a multi-line `&str` of CSV data (name,age,city), splits it into lines, splits each line by commas, and extracts the names (first field) into a `Vec<String>`. Use `.lines()`, `.split(',')`, and `.trim()`. Focus on when you need to convert `&str` slices into owned `String` values (e.g., when collecting into the Vec) and when you can work with borrowed `&str` slices
- [ ] **Conversion fluency**: Write a program that demonstrates all 4 ways to convert `&str` to `String` (`.to_string()`, `.to_owned()`, `String::from()`, `.into()`) and all 3 ways to convert `String` to `&str` (`&s`, `&s[..]`, `.as_str()`). For each, write a brief comment explaining when you'd prefer one over another

## Notes
- ~1-1.5 hours estimated
- Continues in 018b (UTF-8 and string manipulation)
