# Lesson 117: Completion and Polish

## Section 21: Capstone Projects

## Status: pending

## Prerequisites
- Lesson 116 (Architecture and Core Implementation)

## Added
- Split from lesson 116 (v6 pacing review)

## Objectives
- [ ] Complete the core implementation: finish remaining operations and ensure all public API methods work correctly
- [ ] Add error handling: define and use proper error types for all failure modes, ensure no panics in public API
- [ ] Write comprehensive tests: add 3-5 more tests including edge cases and error conditions
- [ ] (Optional) Add one unsafe optimization with SAFETY comments, or add proptest for a key property invariant

## Exercises
- [ ] **Exercise 1 -- Complete functionality**: Finish the remaining operations. For Option A: implement `spawn` and `block_on` that can drive at least 2 tasks to completion. Use the provided Waker scaffold below -- the `signal_waker` function is partially provided; complete it using the RawWaker pattern from lesson 074, then use it in your spawn/block_on implementation.
  ```rust
  // Provided: Simple waker that signals readiness via an Arc<AtomicBool>
  use std::sync::{Arc, atomic::{AtomicBool, Ordering}};
  use std::task::{RawWaker, RawWakerVTable, Waker};

  struct Signal(AtomicBool);

  impl Signal {
      fn new() -> Arc<Self> { Arc::new(Signal(AtomicBool::new(false))) }
      fn is_woken(&self) -> bool { self.0.load(Ordering::SeqCst) }
      fn reset(&self) { self.0.store(false, Ordering::SeqCst); }
  }

  // Convert Arc<Signal> into a Waker — you may use this as-is
  fn signal_waker(signal: Arc<Signal>) -> Waker {
      // Implementation hint: use RawWaker + RawWakerVTable
      // The wake function should set the AtomicBool to true
      // Reminder: The RawWaker pattern uses Arc::into_raw, Arc::from_raw,
      // and a RawWakerVTable with clone/wake/wake_by_ref/drop functions
      // (see lesson 074).
      todo!("Implement using the pattern from lesson 074")
  }
  ```
  For Option B: implement the Parser that builds an AST from tokens, and a simple evaluator. _Evaluator scope: integers and basic arithmetic (+, -, *, /) only. Parentheses for grouping. Do not implement variables, functions, or string operations._ For Option C: implement `get`, `contains`, and iteration (via `IntoIterator` or an `iter()` method).
- [ ] **Exercise 2 -- Edge cases and error handling**: Add 3-5 more tests covering edge cases: large inputs, error conditions, boundary values. Ensure all public API methods return `Result` or handle errors gracefully rather than panicking. For Option B: test malformed input. For Option C: test duplicate keys, missing keys.
- [ ] **Exercise 3 -- (Optional) Advanced polish**: Choose one: (a) Add one `unsafe` optimization with detailed `// SAFETY:` comments explaining the invariant (e.g., unchecked indexing in a hot path, or raw pointer manipulation in the data structure). (b) Add a proptest property test for a key invariant (e.g., "insert then get always returns the value", "parsed then displayed AST re-parses to same result").

## Notes
_Lesson not yet started._
_Split from original lesson 116 which was rated OVERLOADED (~3-5 hr). This part completes the project started in 116._
_Exercise 3 is optional -- the core goal is a working, tested implementation. The unsafe/proptest polish is a stretch goal._
