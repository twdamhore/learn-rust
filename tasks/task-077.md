# Lesson 077: Associated types, GATs (generic associated types)

## Section 17: Advanced Type System

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Understand associated types in traits (`type Item`) and how they differ from generic type parameters on the trait itself
- [ ] Compare when to use associated types vs type parameters by examining real std traits (`Iterator`, `Add`, `Deref`) and articulating the "one impl per type" rule
- [ ] Understand GATs (generic associated types) -- what they are, why they were stabilized, and the problems they solve (lending iterators, async-in-traits return types)
- [ ] Write a GAT-based trait that returns references tied to `&self` lifetime (a lending iterator pattern), something impossible with plain associated types
- [ ] Recognize the compile errors you get when you need a GAT but use a plain associated type, and know how to refactor

## Exercises
- [ ] **Exercise 1 -- Graph trait with associated types**: Define a `trait Graph { type Node; type Edge; ... }` with methods `nodes(&self) -> Vec<Self::Node>` and `edges(&self, from: &Self::Node) -> Vec<Self::Edge>`. Implement it for an adjacency-list struct. Compare this design to `trait Graph<N, E>` and explain why associated types are better here.
- [ ] **Exercise 2 -- Refactor generic to associated**: Start with `trait Storage<K, V> { fn get(&self, key: &K) -> Option<&V>; }` where K and V are type parameters. Refactor to use associated types instead. Discuss: when would you keep the generics?
- [ ] **Exercise 3 -- Iterator-like trait**: Implement `trait Summarizable { type Summary: Display; fn summarize(&self) -> Self::Summary; }` for at least two different types (e.g., `Article` returns `String`, `Tweet` returns a custom `TweetSummary` struct). Write a generic function `fn print_summary<T: Summarizable>(item: &T)` that works with any implementor.
- [ ] **Exercise 4 [STRETCH] -- Lending iterator with GATs**: _You'll rarely write GATs yourself, but understanding them helps when you encounter them in libraries like lending iterators, async traits, and database query builders._ Implement a `WindowsMut` struct that yields overlapping mutable slices from a `Vec<i32>`. Use the provided trait definition below and implement it for `WindowsMut`. Verify that this cannot be done with the standard `Iterator` trait.
  ```rust
  // Provided trait definition — implement this for WindowsMut
  trait LendingIterator {
      type Item<'a> where Self: 'a;
      fn next(&mut self) -> Option<Self::Item<'_>>;
  }
  ```

## Notes
_Lesson not yet started._
