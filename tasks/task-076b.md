# Lesson 076b: FFI - Part B: Exposing Rust to Python (PyO3)

## Section 16: Unsafe & FFI

## Status: pending

## Prerequisites
- Python 3 installed
- pip available
- Create and activate a virtual environment first: `python3 -m venv .venv && source .venv/bin/activate`

## Added
- Split from lesson 076 (v6 pacing review)

## Objectives
- [ ] Set up PyO3 with maturin for building Python extensions in Rust
- [ ] Expose Rust functions to Python using `#[pyfunction]` and `#[pymodule]`
- [ ] Expose Rust structs as Python classes using `#[pyclass]` with `#[pymethods]`

## Exercises
- [ ] **PyO3 setup and first function**: Set up `maturin` (`pip install maturin`), create a PyO3 project with `maturin init`, expose a simple `#[pyfunction] fn fibonacci(n: u64) -> u64` to Python; build with `maturin develop` and test from a Python script
- [ ] **Rust struct as Python class**: Expose a Rust struct `Counter` as a `#[pyclass]` with `increment`, `decrement`, and `get` methods via `#[pymethods]`; add `__repr__` for Python string representation; test from Python
- [ ] **Performance comparison**: Compare performance of pure Python vs Rust-backed Python for a compute-heavy task (e.g., fibonacci, prime sieve, or matrix operations); time both implementations from Python and observe the speedup

## Notes
_Lesson not yet started._
