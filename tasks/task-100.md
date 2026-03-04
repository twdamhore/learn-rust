# Lesson 100: Project 3 - continued (unsafe where needed, optimization, benchmarks)

## Section 21: Capstone Projects

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Set up benchmarks using `criterion` for all performance-critical operations in your capstone 3 project, establishing a baseline for optimization
- [ ] Profile the project using `cargo flamegraph` or `perf` to identify hot paths and bottlenecks, then apply targeted optimizations
- [ ] Audit all `unsafe` blocks for soundness: verify each one is necessary, document the safety invariant it relies on, and add `// SAFETY:` comments explaining why the code is correct
- [ ] Write comprehensive documentation: crate-level docs (`//!`), module docs, public API docs with examples, and a README explaining what the project does and how to use it
- [ ] Reflect on the full 100-lesson journey: identify which Rust concepts were hardest coming from Java/Go, which patterns are now natural, and what areas to explore next

## Exercises
- [ ] Add `criterion` benchmarks for your project: benchmark at least 3 operations at different input sizes (small, medium, large) -- for the executor, benchmark task throughput; for the parser, benchmark parsing speed on varying expression complexity; for the B-tree, benchmark insert/get/remove at different tree sizes; compare at least one operation against a standard library equivalent (e.g., `BTreeMap` vs your B-tree)
- [ ] Generate a flamegraph of a realistic workload, identify the top 3 hottest functions, and implement at least one optimization (e.g., reducing allocations, improving cache locality, avoiding unnecessary clones) -- re-benchmark to measure the improvement and document what you changed and why
- [ ] Review every `unsafe` block in your project: for each one, write a `// SAFETY:` comment explaining the invariant, consider whether a safe alternative exists, and write a test that would catch undefined behavior if the safety invariant were violated (e.g., using Miri with `cargo +nightly miri test` if possible)
- [ ] Write a "lessons learned" retrospective (as comments in your `main.rs` or a dedicated module): list the top 10 Rust concepts that were most different from Java/Go, the 5 most useful patterns you learned, and 3 areas you want to explore further (e.g., embedded, advanced async, contribution to open-source Rust projects)

## Notes
_**SUPERSEDED**: This lesson has been split into [Lesson 100a](task-100a.md) and [Lesson 100b](task-100b.md). Use those files instead._

_Lesson not yet started._
