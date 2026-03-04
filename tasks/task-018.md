# Lesson 018: Strings in Rust for Java/Go devs - String, &str, when to use which

## Section 4: Strings & Slices

## Status: pending

## Added
- Initial curriculum design [NEW - bridging lesson]

## Objectives
- [ ] Understand `String` vs `&str` thoroughly: `String` is an owned, growable, heap-allocated UTF-8 string; `&str` is a borrowed, immutable view into UTF-8 bytes (either heap-allocated String data, static binary data, or a slice of either)
- [ ] Know when to use each in function signatures: accept `&str` for read-only access (most common), accept `String` when the function needs to own/store the data, return `String` when creating new string data, return `&str` when returning a slice of input
- [ ] Understand UTF-8 implications: Rust strings are not indexable by character position (`s[0]` does not compile), `.len()` returns byte count not character count, `.chars()` iterates by Unicode scalar value, multi-byte characters affect slicing
- [ ] Convert fluently between `String` and `&str`: `&str` to `String` via `.to_string()`, `.to_owned()`, `String::from()`, or `.into()`; `String` to `&str` via `&s`, `&s[..]`, or `.as_str()`
- [ ] Know essential string methods: `.contains()`, `.starts_with()`, `.find()`, `.replace()`, `.trim()`, `.split()`, `.chars()`, `.push_str()`, `.push()`, `format!()` for building strings

## Exercises
- [ ] **Function signature practice**: Write these functions with the most idiomatic signature: (1) `is_palindrome` - checks if a string reads the same forwards and backwards, (2) `make_uppercase` - returns a new uppercase string, (3) `greet` - takes a name and returns "Hello, {name}!", (4) `add_greeting` - takes a mutable `Vec<String>` and a name, pushes "Hello, {name}!" into the Vec (shows when a function needs to own a `String`). For each, explain in comments why you chose `&str` vs `String` for the parameter and return type
- [ ] **String processing pipeline**: Build a function that takes a multi-line `&str` of CSV data (name,age,city), splits it into lines, splits each line by commas, and extracts the names (first field) into a `Vec<String>`. Use `.lines()`, `.split(',')`, and `.trim()`. Focus on when you need to convert `&str` slices into owned `String` values (e.g., when collecting into the Vec) and when you can work with borrowed `&str` slices
- [ ] **UTF-8 exploration**: Create strings containing ASCII ("Hello"), accented characters ("cafe\u{0301}"), emoji ("Hello "), and CJK characters ("Hello"). For each, print: `.len()` (bytes), `.chars().count()` (scalar values), and iterate with `.char_indices()` showing each character's byte offset. Compare with Java's `.length()` (UTF-16 code units) and Go's `len()` (bytes) vs `utf8.RuneCountInString()` (runes)
- [ ] **Word counter**: Implement a word-frequency counter using `HashMap`. Count how many times each word appears in a given `&str` (use `.split_whitespace()`). Note the ownership challenge: `.to_lowercase()` returns a `String`, but using `&str` as keys borrows from the input — solve this by using `HashMap<String, usize>` with owned keys. Write both a case-sensitive version (keys borrow from input: `HashMap<&str, usize>`) and a case-insensitive version (keys are owned: `HashMap<String, usize>`), and compare the tradeoffs in comments

  > **Scaffolding**: `HashMap` is covered fully in lesson 36. For now, use this template:
  >
  > ```rust
  > use std::collections::HashMap;
  >
  > let mut map = HashMap::new();
  > map.insert("key", 1);            // insert a key-value pair
  > let count = map.entry("key").or_insert(0);  // get or create entry
  > *count += 1;                      // modify the value
  > ```

## Notes
**SUPERSEDED**: This lesson was split into task-018a.md (String vs &str, when to use which) and task-018b.md (UTF-8 and string manipulation) during the v13 pacing review on 2026-03-04. The original was ~2+ hours with a HashMap forward reference and 4 substantial exercises.

_Lesson not yet started._
