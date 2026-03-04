# Lesson 091: no_std - embedded basics, core vs std

## Section 20: Special Targets

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Understand what `#![no_std]` removes from the default environment: the `std` crate (heap allocation, I/O, threading, networking) and why `core` remains available with all language primitives (Option, Result, iterators, traits)
- [ ] Know the role of the `alloc` crate as a middle ground -- heap allocation (Vec, String, Box, Rc) without the full std library, and how to use it with `extern crate alloc`
- [ ] Write `no_std`-compatible library code using only `core` types and traits, understanding which common features are and are not available
- [ ] Use conditional compilation to make a crate work in both `std` and `no_std` environments using Cargo features (e.g., a default `std` feature that falls back to `core`)
- [ ] Understand real-world `no_std` use cases: embedded systems (microcontrollers), WebAssembly modules, OS kernels, and bootloaders -- and how this compares to Go's single-runtime approach that makes bare-metal Go impractical

## Exercises
- [ ] **Exercise 1 -- no_std Fixed-Size Stack**: Create a `#![no_std]` library crate that implements a fixed-size stack (`ArrayStack<T, const N: usize>`) using only `core` types -- support `push`, `pop`, `peek`, `is_empty`, and `len`, with no heap allocation
- [ ] **Exercise 2 -- Conditional std Feature**: Add a Cargo feature called `std` (set as default) to the library: when enabled, implement `std::error::Error` for your error type and provide `Display`; when disabled, use `core::fmt::Display` only -- use `#[cfg(feature = "std")]` to gate the std-dependent code
- [ ] **Exercise 3 -- alloc-Based SortedVec**: **Note on `extern crate alloc`**: In `no_std` code, the standard library's prelude is not available, so `Vec`, `String`, `Box`, etc. are not automatically imported. The `extern crate alloc;` declaration makes the `alloc` crate available, giving you access to heap-allocated types via `use alloc::vec::Vec;` etc. This `extern crate` syntax is rarely needed in normal Rust (the 2018 edition made it mostly unnecessary) but is still required for `alloc` in `no_std` contexts. Write a second `no_std` library that uses `extern crate alloc` to provide a `SortedVec<T: Ord>` type backed by `alloc::vec::Vec` -- implement insert (maintaining sort order), contains (binary search), and iteration
- [ ] **Exercise 4 -- Testing no_std Libraries**: Write tests for both libraries: test the `no_std` + `core`-only library with `--no-default-features` to verify it compiles without std, and test the `alloc`-based library to verify heap-backed functionality works correctly

## Notes
_Lesson not yet started._
