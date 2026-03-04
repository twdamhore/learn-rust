# Lesson 099: Project 3 - Systems tool (async runtime piece OR parser OR custom data structure)

## Section 21: Capstone Projects

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Choose one of three systems projects based on interest: (A) a simple async task scheduler/executor, (B) a recursive descent parser for a small language, or (C) a custom B-tree data structure -- and document the design rationale
- [ ] Design the architecture: define public API, internal data structures, error types, and module boundaries before writing implementation code
- [ ] Implement the core logic using advanced Rust features from the curriculum: generics, trait bounds, lifetimes, smart pointers, and iterators as appropriate to the chosen project
- [ ] Use `unsafe` only where genuinely needed (e.g., raw pointer manipulation in the data structure, or low-level runtime mechanics in the executor) and wrap all unsafe code in safe abstractions with documented safety invariants
- [ ] Write thorough tests covering normal operation, edge cases, and error conditions from the start -- use TDD where practical

## Exercises
- [ ] **Option A (Task Scheduler)**: Implement a single-threaded async task executor with a task queue, a `spawn` function that takes a `Future + 'static`, a `block_on` function that drives futures to completion, and a `Waker` implementation that re-queues tasks -- support at least 3 tasks running concurrently via cooperative multitasking
- [ ] **Option B (Parser)**: Implement a recursive descent parser for a simple expression language supporting: integers, identifiers, arithmetic (+, -, *, / with precedence), parentheses, let bindings (`let x = 5`), and if/else -- produce an AST (defined as an enum), implement `Display` for pretty-printing, and write an evaluator that walks the AST
- [ ] **Option C (B-Tree)**: Implement a generic `BTree<K: Ord, V>` with configurable order: support `insert`, `get`, `contains_key`, `remove`, and in-order iteration via `IntoIterator` -- handle node splitting and merging correctly, and use `unsafe` for the internal node structure if needed (with safe public API)
- [ ] Whichever option you choose: write at least 15 tests covering normal cases, edge cases (empty input, single element, maximum capacity), and error cases -- include property-based tests using `proptest` for at least one invariant (e.g., "inserting then getting always returns the value" or "parsed then displayed AST re-parses to the same result")

## Notes
_**SUPERSEDED**: This lesson has been split into [Lesson 99a](task-099a.md) and [Lesson 99b](task-099b.md). Use those files instead._

_Lesson not yet started._
