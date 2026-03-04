# Lesson 076: FFI - exposing Rust to C/Python, cbindgen, PyO3

## Section 16: Unsafe & FFI

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Use `#[no_mangle]` and `extern "C"` to export Rust functions with C-compatible ABI
- [ ] Generate C header files from Rust code using `cbindgen`
- [ ] Understand `PyO3` basics for creating Python modules from Rust (`#[pyfunction]`, `#[pymodule]`, `#[pyclass]`)
- [ ] Handle memory ownership across FFI boundaries: who allocates, who frees, and how to avoid leaks or double-frees

## Exercises
- [ ] **Export Rust to C**: Write a Rust library (`crate-type = ["cdylib"]`) that exports `extern "C" fn add(a: i32, b: i32) -> i32` and `extern "C" fn greet(name: *const c_char)` (prints a greeting); compile it and verify the symbols exist with `nm` or `objdump`
- [ ] **Generate C header with cbindgen**: Add `cbindgen` to the project from the previous exercise; configure `cbindgen.toml` and a `build.rs` that generates a `.h` file; inspect the generated header and verify it matches the exported functions
- [ ] **PyO3 Python module**: Create a new crate with `pyo3` and `maturin`; implement a `#[pyfunction] fn fibonacci(n: u64) -> u64` and a `#[pyclass] struct Counter` with `increment` and `get` methods; build with `maturin develop` and test from Python
- [ ] **FFI memory ownership**: Write an `extern "C" fn create_string() -> *mut c_char` that allocates a `CString` and returns ownership to C (using `into_raw`), and an `extern "C" fn free_string(ptr: *mut c_char)` that reclaims and drops it (using `from_raw`); document the ownership contract; write a Rust test that exercises the allocate-then-free cycle

## Notes
_**SUPERSEDED**: This lesson has been split into [Lesson 76a](task-076a.md) and [Lesson 76b](task-076b.md). Use those files instead._

_Lesson not yet started._
