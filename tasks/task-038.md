# Lesson 038: HashMap, HashSet, BTreeMap, entry API

## Section 8: Collections & Iterators

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Create and use `HashMap<K, V>` with `insert`, `get`, `remove`, `contains_key`, and iteration
- [ ] Use the entry API: `entry().or_insert()`, `entry().or_insert_with()`, and `entry().and_modify().or_insert()` for conditional insertion and update
- [ ] Understand that `HashMap` keys must implement `Hash + Eq`, and know which standard types satisfy this (and that `f64` does not)
- [ ] Use `HashSet<T>` for storing unique values and performing set operations (intersection, union, difference, symmetric_difference)
- [ ] Use `BTreeMap<K, V>` when you need sorted key order, and understand its `Ord` requirement vs HashMap's `Hash + Eq`

## Exercises
- [ ] **Exercise 1 - Word frequency counter**: Write `fn word_count(text: &str) -> HashMap<String, usize>` that counts occurrences of each word (case-insensitive). Test with `"the cat sat on the mat the cat"` expecting `{"the": 3, "cat": 2, "sat": 1, "on": 1, "mat": 1}`
- [ ] **Exercise 2 - Entry API mastery**: Rewrite the word counter using `entry().and_modify(|c| *c += 1).or_insert(1)`. Then write a function that groups words by their first letter using `entry().or_insert_with(Vec::new)` to build a `HashMap<char, Vec<String>>`
- [ ] **Exercise 3 - Simple cache**: Implement a `Cache` struct wrapping a `HashMap<String, String>` with methods `get(&self, key: &str) -> Option<&String>`, `set(&mut self, key: String, value: String)`, and `get_or_insert(&mut self, key: String, value: String) -> &String`. Implement a `get_or_insert` method that takes a key and a default value (both `String`), returning a reference to the existing or newly inserted value. Test that calling `get_or_insert` with an existing key returns the original value, not the new default. (We use concrete `String` types here; generics are introduced in lesson 39. A more advanced version using closures (`FnOnce`) is covered after lesson 055.)
- [ ] **Exercise 4 - Sets and sorted maps**: Given two `Vec<String>` representing students in two classes, use `HashSet` to find students in both classes (intersection), students in either (union), and students in only one class (symmetric difference). Then use `BTreeMap` to print all word counts from Exercise 1 in alphabetical order

## Notes
_Lesson not yet started._

> **Pacing note**: Lessons 038-037-038 (collections, iterators, custom iterators) form a dense cluster. If you feel fatigued after this lesson, take a break before continuing to lesson 039. These three lessons cover foundational patterns you'll use constantly, so it's worth taking the time to absorb them.
