# Lesson 018b: Strings Part B - UTF-8 and String Manipulation

## Section 4: Strings & Slices (split from lesson 018)

## Status: pending

## Added
- Split from task-018 (v13 pacing review, 2026-03-04)

## Objectives
- [ ] Understand UTF-8 implications: Rust strings are not indexable by character position (`s[0]` does not compile), `.len()` returns byte count not character count, `.chars()` iterates by Unicode scalar value, multi-byte characters affect slicing
- [ ] Know essential string methods: `.contains()`, `.starts_with()`, `.find()`, `.replace()`, `.trim()`, `.split()`, `.chars()`, `.push_str()`, `.push()`, `format!()` for building strings

## Exercises
- [ ] **UTF-8 exploration**: Create strings containing ASCII ("Hello"), accented characters ("cafe\u{0301}"), emoji ("Hello 🌍"), and CJK characters ("你好"). For each, print: `.len()` (bytes), `.chars().count()` (scalar values), and iterate with `.char_indices()` showing each character's byte offset. Compare with Java's `.length()` (UTF-16 code units) and Go's `len()` (bytes) vs `utf8.RuneCountInString()` (runes)
- [ ] **String methods practice**: Write a `clean_and_split` function that takes a `&str`, trims whitespace, converts to lowercase, splits on commas, trims each part, and collects into `Vec<String>`. Then write a `find_and_replace` function that replaces all occurrences of a word in a `&str`. Test both with various inputs
- [ ] **Word counter [STRETCH]**: Implement a word-frequency counter using `HashMap<String, usize>`. Count how many times each word appears in a given `&str` (use `.split_whitespace()` and `.to_lowercase()`). Note the ownership challenge: `.to_lowercase()` returns a `String`, so keys must be owned

  > **Scaffolding**: `HashMap` is covered fully in lesson 36. For now, use this template:
  >
  > ```rust
  > use std::collections::HashMap;
  >
  > let mut map = HashMap::new();
  > let count = map.entry(word).or_insert(0);
  > *count += 1; // `or_insert(0)` returns `&mut usize` (a mutable reference to the value). `*count` dereferences it to modify the value in place.
  > ```

## Notes
- ~1-1.5 hours estimated
- Prerequisite: 018a (String vs &str fundamentals)
