# Lesson 018: Slices - string slices, array slices, &str vs String

## Section 4: Strings & Slices

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Understand slices as fat pointers (pointer + length) that provide a view into a contiguous sequence of elements without owning them
- [ ] Create string slices (`&str`) from `String` using range indexing (`&s[0..5]`, `&s[..]`) - understand that string slices must land on valid UTF-8 character boundaries
- [ ] Create array and Vec slices (`&[T]`) using range syntax - know that `&v[1..4]` gives a slice of 3 elements, `&v[..]` gives the full slice
- [ ] Understand the parallel relationships: `String` owns heap data / `&str` borrows it, `Vec<T>` owns heap data / `&[T]` borrows it - slices are the borrowed form of owned collections
- [ ] Know that `&str` and `&[T]` are the idiomatic parameter types for functions that only need to read string or sequence data (not `&String` or `&Vec<T>`)

## Exercises

> **Preview**: `Option<T>` is Rust's way of representing "might not have a value" — it's either `Some(value)` or `None`. Covered fully in lesson 22.

- [ ] **First word finder**: Write a function `fn first_word(s: &str) -> &str` that returns a slice of the first word (up to the first space, or the whole string if no space). Test it with both `String` values (passing `&my_string`) and string literals (which are already `&str`). [STRETCH] Then extend it to `fn nth_word(s: &str, n: usize) -> Option<&str>`
- [ ] **Array slice operations**: Write a function `fn sum_slice(numbers: &[i32]) -> i32` that sums a slice. Call it with: a full array `&arr`, a partial array `&arr[1..3]`, a full Vec `&vec`, and a partial Vec `&vec[2..]`. Verify they all work with the same function. Then write `fn largest(list: &[i32]) -> Option<&i32>` that returns a reference to the largest element
- [ ] **UTF-8 boundary panic**: Create a String containing a multi-byte character (e.g., `"Hello, world"` with an emoji or `"Zdravo"` with Cyrillic). Try to slice it at a byte position that falls in the middle of a multi-byte character - observe the panic. Then write a safe version using `.char_indices()` that slices at character boundaries
- [ ] **Slice vs owned comparison**: Write two versions of a function that extracts the domain from an email address - one returning `String` (using allocation) and one returning `&str` (using slicing). Write comments comparing: Which is more efficient? When would you need the String version? Connect this to Java's `substring()` (which used to share the backing array pre-Java 7u6, then switched to copying)

    > **Hint**: `.find('@')` returns `Option<usize>` — the byte index of `'@'` if found, or `None`. `Option` was previewed at the top of this lesson and is covered fully in lesson 22.

## Notes
_Lesson not yet started._
