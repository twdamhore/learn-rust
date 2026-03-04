# Lesson 084a: Benchmarking Part A: Criterion and Measurement

## Section 18: Testing & Quality

## Status: pending

## Added
- Split from task-084 during v7 review due to heavy pacing (~2+ hr estimated)
- Part A focuses on criterion benchmarks, comparing algorithms, debug vs release, and compiler flags (~1-1.5 hr)

## Objectives
- [ ] Set up the `criterion` crate for micro-benchmarking and understand its statistical approach (warm-up, sample collection, confidence intervals) vs naive timing
- [ ] Interpret criterion benchmark results: mean, median, standard deviation, throughput, and comparison with previous runs (regression detection)
- [ ] Write parameterized benchmarks that compare multiple implementations across different input sizes
- [ ] Understand the impact of optimization levels (`--release` vs debug), LTO, `codegen-units`, and `opt-level` on performance

## Exercises
- [ ] **Exercise 1 -- Criterion benchmark**: Create two implementations of "find all duplicates in a Vec<i32>": one using nested loops (O(n^2)) and one using a HashSet (O(n)). Write criterion benchmarks for both with input sizes of 100, 1000, and 10000 elements. Run `cargo bench`, interpret the HTML report criterion generates, and document the performance difference.
- [ ] **Exercise 2 -- Debug vs release comparison**: Take the duplicate-detection implementations from Exercise 1 and benchmark them in both debug and release mode. Document the performance difference. Then experiment with these `Cargo.toml` profile settings and create a table showing how each affects runtime for the 10000-element input:

  ```toml
  [profile.release]
  opt-level = 3        # max optimization (try 0, 1, 2, 3)
  lto = true           # link-time optimization (try false, true, "thin")
  codegen-units = 1    # single codegen unit for better optimization
  # target-cpu = "native"  # uncomment in RUSTFLAGS, not Cargo.toml
  ```
  > **Tip**: To set `target-cpu=native`, use: `RUSTFLAGS="-C target-cpu=native" cargo bench`

## Notes
- This lesson pairs with lesson 084b which covers profiling and flamegraphs.
- Exercise 2 builds directly on Exercise 1 -- complete Exercise 1 first.
- The `criterion` crate generates HTML reports in `target/criterion/` -- open them in a browser for detailed visualizations.
- If `cargo bench` seems slow on debug builds, that is expected and part of the lesson.
_Lesson not yet started._
