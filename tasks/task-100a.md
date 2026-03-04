# Lesson 100a: Project 3 Part C: Benchmarking and Optimization

## Section 21: Capstone Projects

## Status: pending

## Prerequisites
- Lesson 099b (Capstone Project 3 - Part B: Completion and Polish)
- Lessons 084a/084b (Benchmarking - criterion, profiling, flamegraphs)

## Added
- Split from lesson 100 (v7 pacing review)

## Objectives
- [ ] Set up `criterion` benchmarks for all performance-critical operations in your capstone 3 project, establishing a baseline for optimization
- [ ] Benchmark at least 3 operations at different input sizes (small, medium, large) and compare at least one against a standard library equivalent
- [ ] Profile the project using `cargo flamegraph` or `perf` to identify hot paths and bottlenecks
- [ ] Apply at least one targeted optimization based on profiling results (e.g., reducing allocations, improving cache locality, avoiding unnecessary clones)
- [ ] Re-benchmark after optimization and document before/after measurements

## Exercises
- [ ] **Exercise 1 -- Criterion benchmarks**: Add `criterion` benchmarks for your project: benchmark at least 3 operations at different input sizes (small, medium, large). For the executor: benchmark task throughput. For the parser: benchmark parsing speed on varying expression complexity. For the B-tree: benchmark insert/get/remove at different tree sizes. Compare at least one operation against a standard library equivalent (e.g., `BTreeMap` vs your B-tree, `std` parser vs yours).
- [ ] **Exercise 2 -- Flamegraph and optimization**: Generate a flamegraph of a realistic workload using `cargo flamegraph` (requires `perf` on Linux or `dtrace` on macOS). Identify the top 3 hottest functions. Implement at least one optimization targeting a hot path (e.g., reducing allocations, caching results, replacing `clone()` with references, using `Vec::with_capacity`). Re-run benchmarks and document: what you changed, why, and the before/after measurements.

## Notes

> **Benchmark comparison targets by option:**
> - Option A (executor): Compare your `spawn` + `block_on` throughput against `tokio::spawn`
> - Option B (parser): Compare your parser against the `nom` crate on the same input
> - Option C (data structure): Compare your implementation against `std::collections::BTreeMap` (or `BinaryHeap`)

_Lesson not yet started._
_Split from original lesson 100 which was assessed as >2 hrs because benchmarking, profiling, and unsafe auditing are each time-consuming activities._
_This part focuses exclusively on performance: establishing benchmarks, profiling, optimizing, and measuring improvement._
_`cargo flamegraph` requires `perf` (Linux) or `dtrace` (macOS) to be installed._

> **Linux setup for profiling:**
> ```bash
> sudo apt install linux-tools-generic linux-tools-$(uname -r)
> # Allow perf for non-root users:
> echo 1 | sudo tee /proc/sys/kernel/perf_event_paranoid
> # Install cargo-flamegraph:
> cargo install flamegraph
> ```
> On macOS, `dtrace` is available by default but may require SIP adjustments.
