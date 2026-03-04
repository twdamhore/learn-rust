# Lesson 104: Rust to WASM Basics

## Section 20: Special Targets

## Status: pending

## Added
- Split from lesson 104 (v6 pacing review)

## Objectives
- [ ] Install `wasm-pack` and add the `wasm32-unknown-unknown` target with `rustup target add wasm32-unknown-unknown`
- [ ] Understand what WebAssembly is and why Rust-to-WASM is a strong use case: near-native performance, small binary size, no garbage collector overhead -- compare with Go's WASM which bundles the entire Go runtime
- [ ] Build a Rust library as a WASM module using `wasm-pack build --target web` and understand the generated output (`.wasm` binary, JS glue code, TypeScript types)
- [ ] Test WASM output with `wasm-pack test --node` to verify correctness from the Rust side without needing a browser

## Exercises
- [ ] **Exercise 1 -- WASM hello world**: Use `wasm-pack new` to scaffold a project. Write a Rust function annotated with `#[wasm_bindgen]` that takes two `u32` arguments and returns their GCD using Euclid's algorithm. Build with `wasm-pack build --target web`. Run `wasm-pack test --node` to verify correctness.
- [ ] **Exercise 2 -- String processing as WASM**: Build a string processing library as WASM: implement a `slugify(input: &str) -> String` function that converts text to URL-friendly slugs (lowercase, replace spaces with hyphens, remove special characters). Add `#[wasm_bindgen]` and test from the Rust side with `wasm-pack test --node`.
- [ ] **Exercise 3 -- Explore WASM output**: Build your library in both debug and release mode. Compare the `.wasm` file sizes. Try adding `wasm-opt` optimization (via `wasm-pack build --release`). Document the size differences and what `wasm-pack` generates in the `pkg/` directory.

## Notes
_Lesson not yet started._
_Split from original lesson 104 which covered WASM basics through browser integration (~2.5-3.5 hr estimated). This part focuses on Rust-side WASM tooling without requiring browser/JS knowledge._
