_**SUPERSEDED**: This lesson has been split into [Lesson 84a](task-084a.md) and [Lesson 84b](task-084b.md). Use those files instead._

# Lesson 084: Benchmarking - criterion, profiling, flamegraphs

## Section 18: Testing & Quality

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Set up the `criterion` crate for micro-benchmarking and understand its statistical approach (warm-up, sample collection, confidence intervals) vs naive timing
- [ ] Interpret criterion benchmark results: mean, median, standard deviation, throughput, and comparison with previous runs (regression detection)
- [ ] Use `perf` (or equivalent) and `cargo-flamegraph` to generate flamegraphs that visually show where time is spent in a program
- [ ] Identify hot spots from profiling data and apply targeted optimizations (algorithmic changes, allocation reduction, cache-friendly access patterns)
- [ ] Understand the impact of optimization levels (`--release` vs debug), LTO, codegen-units, and PGO on performance

## Exercises
- [ ] **Exercise 1 -- Criterion benchmark**: Create two implementations of "find all duplicates in a Vec<i32>": one using nested loops (O(n^2)) and one using a HashSet (O(n)). Write criterion benchmarks for both with input sizes of 100, 1000, and 10000 elements. Run `cargo bench`, interpret the HTML report criterion generates, and document the performance difference.
- [ ] **Exercise 2 -- Flamegraph**: Write a program that builds a large `HashMap<String, Vec<u64>>` (100K entries, each with 100 values), then iterates all values to compute a sum. Generate a flamegraph with `cargo flamegraph`. Identify the hottest functions. Optimize by switching to `FxHashMap` or pre-allocating capacity, re-profile, and compare the flamegraphs.
- [ ] **Exercise 3 -- Optimization from profiling**: Write a deliberately slow `fn process_text(input: &str) -> HashMap<String, usize>` that counts word frequencies using unnecessary allocations (e.g., `to_uppercase()` on every comparison, cloning strings needlessly). Benchmark it with criterion. Profile to identify waste. Optimize step by step (reuse allocations, use `&str` keys, avoid redundant work). Show benchmark improvement at each step.
- [ ] **Exercise 4 -- Debug vs release comparison**: Take the word-frequency counter from Exercise 3 and benchmark it in both debug and release mode. Document the performance difference. Then experiment with `Cargo.toml` settings: `opt-level`, `lto`, `codegen-units = 1`. Create a table showing how each setting affects runtime for a large input.

## Notes
_Lesson not yet started._
