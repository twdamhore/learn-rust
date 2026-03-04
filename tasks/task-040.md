# Lesson 040: Custom iterators, IntoIterator, lazy evaluation

## Section 8: Collections & Iterators

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Implement the `Iterator` trait for a custom struct by defining `type Item` and `fn next(&mut self) -> Option<Self::Item>`
- [ ] Understand the `IntoIterator` trait and how it enables `for item in collection` syntax for custom types
- [ ] Provide `iter()`, `iter_mut()`, and `into_iter()` methods for a custom collection, matching the convention used by `Vec` and other std types
- [ ] Understand that iterator adaptors are zero-cost abstractions: the compiler optimizes chained iterators to be as fast as hand-written loops

---

> **Prerequisite Note: Implementing a Trait**
>
> This lesson requires you to write `impl Iterator for YourType { ... }`, which is Rust's syntax for implementing a trait on a type. The general pattern is: `impl TraitName for TypeName { ... }`, where you provide concrete implementations for the methods the trait requires. You have seen traits used via `#[derive(...)]` in lesson 023, but here you are writing the implementation by hand.
>
> Traits are formally taught in lesson 042, so do not worry about understanding every detail yet. For now, just follow the template below: define `type Item` to declare what your iterator yields, and implement `fn next(&mut self) -> Option<Self::Item>` to produce the next value (or `None` when finished). That is all you need for the exercises in this lesson.

---

### Template: Implementing the Iterator Trait

```rust
struct Counter {
    count: u32,
    max: u32,
}

impl Counter {
    fn new(max: u32) -> Self {
        Counter { count: 0, max }
    }
}

impl Iterator for Counter {
    type Item = u32;  // What type does next() return?

    fn next(&mut self) -> Option<Self::Item> {
        if self.count < self.max {
            self.count += 1;
            Some(self.count)
        } else {
            None
        }
    }
}
```

---

## Exercises
- [ ] **Exercise 1 - Fibonacci iterator**: Create a `Fibonacci` struct and implement `Iterator` for it. It should yield the infinite Fibonacci sequence (0, 1, 1, 2, 3, 5, 8, ...). Use `.take(10).collect::<Vec<u64>>()` to get the first 10 values. Also use `.take_while(|&x| x < 1000)` to get all Fibonacci numbers below 1000
- [ ] **Exercise 2 - Custom collection with IntoIterator**: Create a `Playlist` struct that holds a `Vec<Song>` (where `Song` has `title: String` and `duration_secs: u32`). Implement the consuming `IntoIterator for Playlist` (which takes ownership and doesn't need lifetimes). Demonstrate using `for song in playlist`.

  **Bonus (read-only preview)**: Here's what `IntoIterator for &Playlist` looks like -- we'll understand the `'a` lifetime syntax in lesson 048:
  ```rust
  impl<'a> IntoIterator for &'a Playlist {
      type Item = &'a Song;
      type IntoIter = std::slice::Iter<'a, Song>;
      fn into_iter(self) -> Self::IntoIter {
          self.songs.iter()
      }
  }
  ```
  For now, just implement the consuming `IntoIterator for Playlist` (which takes ownership and doesn't need lifetimes)
- [ ] **Exercise 3 - Prime iterator**: Create a `Primes` struct that implements `Iterator` to yield prime numbers indefinitely. Use the provided trial-division helper below. Use it to collect the first 20 primes, find the first prime above 1000 (with `.find()`), and sum all primes below 100 (with `.take_while().sum()`)

  ```rust
  // Provided: simple primality check
  fn is_prime(n: u64) -> bool {
      if n < 2 { return false; }
      if n < 4 { return true; }
      if n % 2 == 0 || n % 3 == 0 { return false; }
      let mut i = 5;
      while i * i <= n {
          if n % i == 0 || n % (i + 2) == 0 { return false; }
          i += 6;
      }
      true
  }
  // Your job: implement Iterator for a Primes struct that yields consecutive primes
  ```
- [ ] **Exercise 4 [STRETCH] - Iterator vs loop benchmark**: Write a function that sums the squares of even numbers from 1 to 1_000_000 using (a) a `for` loop with `if` and accumulator, and (b) an iterator chain with `.filter().map().sum()`. Use `std::time::Instant` to time both approaches over 100 runs and compare. They should be nearly identical, demonstrating zero-cost abstraction

## Notes
_Lesson not yet started._
