# Lesson 099a: Capstone Project 3 - Part A: Architecture and Core Implementation

## Section 21: Capstone Projects

## Status: pending

## Prerequisites
- Sections 9-12 (generics, traits, lifetimes, closures, smart pointers)
- Section 13-14 (concurrency, async -- for Option A)
- Lesson 083a (proptest -- optional, for property tests)

## Added
- Split from lesson 099 (v6 pacing review)

## Objectives
- [ ] Choose one project option: (A) **[HARD]** a simple async task scheduler/executor piece -- requires deep understanding of Future trait, Waker, and unsafe code, (B) **[MEDIUM]** a recursive descent parser for a small expression language -- familiar pattern for Java developers; well-defined algorithm, or (C) **[MEDIUM-HARD]** a custom data structure (e.g., ordered map or priority queue) -- algorithmic complexity varies by choice. Alternative for Option C: Instead of a B-tree, consider implementing a priority queue (binary heap) -- simpler splitting logic with the same learning goals. Document the choice rationale
- [ ] Design the architecture with clear module boundaries: define the public API, internal data structures, error types, and module layout before writing implementation code
- [ ] Implement core data types and basic operations: get the fundamental types and simplest operations working first
- [ ] Write initial tests using TDD where practical: 5-8 unit tests covering the core functionality

## Exercises
- [ ] **Exercise 1 -- Design document**: Write a design document as comments in `main.rs` or a `design.md`: list the modules, public API functions/methods, key types (structs/enums), and error types. For the chosen option: (A) Task, Executor, Waker types; (B) Token enum, AST enum, Lexer, Parser; (C) Node structure, Tree struct, Iterator.
  > **Example** (Option B): Modules: `lexer`, `parser`, `evaluator`, `ast`. Key types: `Token` enum, `Ast` enum, `ParseError`. Public API: `fn parse(input: &str) -> Result<Ast, ParseError>`, `fn eval(ast: &Ast) -> Result<i64, EvalError>`. This level of detail is sufficient.
- [ ] **Exercise 2 -- Core implementation**: Implement the core types and basic operations. For Option A: Task struct and a basic task queue. For Option B: Token enum and a Lexer that tokenizes simple expressions (numbers, operators, parentheses). For Option C: the data structure with `new()` and `insert()` operations.
- [ ] **Exercise 3 -- Initial tests**: Write 5-8 unit tests for the core functionality implemented in Exercise 2. Cover: basic happy path, empty input, single element, and at least one edge case specific to your option.

## Notes
_Lesson not yet started._
_Split from original lesson 099 which was rated OVERLOADED (~3-5 hr). Architecture guidance is now explicitly provided. Each option is scoped to be achievable in ~2 hours across 099a and 099b combined._
_Reduced from 15+ tests to 5-8 in this part. Focus on getting the design right and core operations working._
