# Lesson 057: Functional patterns - map, filter, fold, method chaining

## Section 11: Closures & Functional Patterns

## Status: pending

> **Note**: This lesson intentionally revisits iterator patterns from lessons 37-38, now combining them with closures for more idiomatic Rust.

## Added
- Initial curriculum design

## Objectives
- [ ] Use `map`, `filter`, `filter_map`, and `fold` on iterators to transform and aggregate data without mutable state
- [ ] Chain multiple iterator adaptors together to build data processing pipelines that are both readable and zero-cost
- [ ] Use `flat_map` to flatten nested structures (e.g., `Vec<Vec<T>>`, `Vec<Option<T>>`) into single iterators
- [ ] Understand how `collect()` uses type inference to produce different collection types (`Vec`, `HashMap`, `String`, `Result<Vec<T>, E>`)
- [ ] Compare Rust iterator chains with Java Streams and Go's manual loop approach, noting Rust's lazy evaluation and zero-cost abstraction advantage

## Exercises
- [ ] **Imperative to functional**: Given a list of `(name: String, age: u32, score: f64)` tuples, rewrite each imperative loop as an iterator chain: (a) filter to people over 18, (b) extract just the names. Verify both versions produce identical results.
- [ ] **fold for aggregation**: Use `fold` to: (a) sum a list of integers, (b) build a `HashMap<char, usize>` counting character frequencies in a string.
- [ ] **flat_map and collect magic**: Given a `Vec<String>` of sentences, use `flat_map` to split each into words and collect all unique words into a `HashSet<&str>`. Then use `collect()` on an iterator of `Result<i32, String>` values to get a `Result<Vec<i32>, String>` -- demonstrate how one `Err` short-circuits the whole collection.
- [ ] **Data pipeline [STRETCH]**: Build a mini data pipeline: read a hardcoded `Vec<&str>` of CSV lines (e.g., `"Alice,85"`, `"Bob,72"`), parse each into a struct, filter by score threshold, sort by name, and format into a result string -- all using iterator chains with no intermediate mutable variables.

## Notes
_Lesson not yet started._
