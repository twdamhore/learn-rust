# Lesson 119: Project 3 Part D: Polish and Retrospective

## Section 21: Capstone Projects

## Status: pending

## Prerequisites
- Lesson 118 (Project 3 Part C: Benchmarking and Optimization)

## Added
- Split from lesson 118 (v7 pacing review)

## Objectives
- [ ] Audit all `unsafe` blocks (if any) for soundness: verify each one is necessary, document the safety invariant, and add `// SAFETY:` comments explaining why the code is correct
- [ ] Run `cargo +nightly miri test` to check for undefined behavior in unsafe code (requires nightly Rust toolchain)
- [ ] Write comprehensive documentation: crate-level docs (`//!`), module docs, public API docs with examples, and a README explaining what the project does and how to use it
- [ ] Reflect on the full 100-lesson journey: identify which Rust concepts were hardest coming from Java/Go, which patterns are now natural, and what areas to explore next

## Exercises
- [ ] **Exercise 1 -- Unsafe audit and Miri**: Review every `unsafe` block in your project (if any exist). For each one, write a `// SAFETY:` comment explaining the invariant, consider whether a safe alternative exists, and write a test that would catch undefined behavior if the safety invariant were violated. Run `cargo +nightly miri test` to verify. If your project has no `unsafe` code, instead: (a) write a small standalone module demonstrating one `unsafe` use case relevant to your project (e.g., unchecked indexing for performance) with full `// SAFETY:` documentation, then (b) verify with Miri that it is sound. Note: Miri requires the nightly Rust toolchain (`rustup toolchain install nightly`).
- [ ] **Exercise 2 -- Documentation and retrospective**: Write comprehensive documentation: crate-level `//!` doc explaining the project purpose, module-level docs, and `///` docs with examples for all public API items. Then write a "lessons learned" retrospective (as comments in `main.rs` or a dedicated `retrospective.md`): list the top 5-10 Rust concepts that were most different from Java/Go, the 3-5 most useful patterns you learned, and 2-3 areas you want to explore further (e.g., embedded Rust, advanced async patterns, contributing to open-source Rust projects).

## Notes
_Lesson not yet started._
_Split from original lesson 118 which was assessed as >2 hrs because benchmarking, profiling, and unsafe auditing are each time-consuming activities._
_This part focuses on code quality and reflection: unsafe auditing, Miri testing, documentation, and a course retrospective._
_If your project has no unsafe code (e.g., parser option), Exercise 1 provides an alternative path._
_Miri requires the nightly Rust toolchain: `rustup toolchain install nightly`._
