# Lesson 039: Iterators - Iterator trait, adaptors, collect, chaining

## Section 8: Collections & Iterators

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Understand the `Iterator` trait: the `next()` method returns `Option<Self::Item>`, and `None` signals the end
- [ ] Use **core** iterator adaptors (master these): `map`, `filter`, `enumerate`, `collect`
- [ ] Be aware of **reference** adaptors (know they exist, look them up when needed): `zip`, `take`, `skip`, `chain`, `flat_map`, `peekable`
- [ ] Use `collect()` to build various collections (`Vec`, `HashMap`, `String`, `HashSet`) from an iterator, with turbofish syntax where needed
- [ ] Chain multiple adaptors together to build data processing pipelines in a single expression
- [ ] Understand iterator laziness: adaptors don't execute until a consuming method (`collect`, `for_each`, `sum`, `count`, `any`, `all`) is called

> **Core adaptors** (master these): `map`, `filter`, `enumerate`, `collect`. The rest are reference -- know they exist, look them up when needed.

## Exercises
- [ ] **Exercise 1 - Transform and collect**: Given `vec![1, 2, 3, 4, 5, 6, 7, 8, 9, 10]`, use `iter().filter().map().collect()` to produce a `Vec<i32>` of the squares of even numbers. Verify the result is `[4, 16, 36, 64, 100]`
- [ ] **Exercise 2 - Chaining adaptors**: Given a `Vec<String>` of lines from a hypothetical file, write a pipeline that: (1) skips the first line (header), (2) filters out empty lines, (3) trims each line, (4) enumerates with line numbers starting at 2, (5) collects into `Vec<(usize, &str)>`. Test with sample input

Note: The `|x| ...` syntax is Rust's closure syntax, similar to Java's `x -> ...` lambdas or Go's `func(x) { ... }` function literals. Full coverage comes in lesson 055.

```rust
// Starter code — complete steps 3-5
let result: Vec<(usize, &str)> = data.iter()
    .skip(1)                          // Step 1: skip header
    .filter(|line| !line.is_empty())  // Step 2: filter empty lines
    // TODO: Step 3 - trim each line
    // TODO: Step 4 - enumerate with line numbers starting at 2
    // TODO: Step 5 - collect into Vec<(usize, &str)>
```
- [ ] **Exercise 3 - Zip and enumerate**: Use `zip` to combine two vectors `names: Vec<&str>` and `scores: Vec<u32>` into a `Vec<(&str, u32)>`. Then use `enumerate` on the result to add rankings. Also use `zip` to build a `HashMap<String, u32>` from the two vectors using `.collect()`
- [ ] **Exercise 4 - Lazy evaluation proof**: Write a custom function `fn noisy_double(x: &i32) -> i32` that prints a message and returns `x * 2`. Use it in a `.map()` chain followed by `.take(3)`. Demonstrate that only 3 calls to `noisy_double` happen (not N), proving laziness. Compare with an imperative loop that processes all elements

## Notes
_Lesson not yet started._
