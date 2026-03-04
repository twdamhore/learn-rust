# Lesson 084b: Benchmarking Part B: Profiling and Optimization

## Section 18: Testing & Quality

## Status: pending

## Added
- Split from task-084 during v7 review due to heavy pacing (~2+ hr estimated)
- Part B focuses on flamegraph generation, profiling-driven optimization, and interpreting profiling results (~1-1.5 hr)

## Objectives
- [ ] Use `perf` (or equivalent) and `cargo-flamegraph` to generate flamegraphs that visually show where time is spent in a program
- [ ] Read and interpret flamegraph output: identify hot functions, understand call stack depth, distinguish application code from library/runtime code
- [ ] Identify hot spots from profiling data and apply targeted optimizations (algorithmic changes, allocation reduction, cache-friendly access patterns)
- [ ] Follow a profiling-driven optimization cycle: measure, identify bottleneck, optimize, re-measure, compare

## Exercises
- [ ] **Exercise 1 -- Flamegraph**: Write a program that builds a large `HashMap<String, Vec<u64>>` (100K entries, each with 100 values), then iterates all values to compute a sum. Generate a flamegraph with `cargo flamegraph`. Identify the hottest functions. Optimize by switching to `FxHashMap` or pre-allocating capacity, re-profile, and compare the flamegraphs.

  FxHashMap comes from the `rustc-hash` crate: `cargo add rustc-hash`, then `use rustc_hash::FxHashMap;`. It's a fast, non-cryptographic hash map used internally by the Rust compiler.
- [ ] **Exercise 2 -- Optimization from profiling**: Write a deliberately slow `fn process_text(input: &str) -> HashMap<String, usize>` that counts word frequencies using unnecessary allocations (e.g., `to_uppercase()` on every comparison, cloning strings needlessly). Benchmark it with criterion (from lesson 084a). Profile to identify waste. Optimize step by step (reuse allocations, use `&str` keys, avoid redundant work). Show benchmark improvement at each step.

## Notes
- This lesson requires lesson 084a to be completed first (criterion knowledge is used in Exercise 2).
- **Platform-specific tooling**: `cargo flamegraph` requires `perf` on Linux (install via `linux-tools-common` / `linux-tools-generic`) or `dtrace` on macOS. On Linux you may also need to set `kernel.perf_event_paranoid` via sysctl.
- Install flamegraph tooling: `cargo install flamegraph`.
- Exercise 2 is iterative -- expect to go through 2-3 optimization rounds. Document each round with before/after benchmark numbers.
_Lesson not yet started._
