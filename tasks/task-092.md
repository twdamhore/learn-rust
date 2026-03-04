# Lesson 092: WebAssembly - wasm-pack, wasm-bindgen, browser integration

## Section 20: Special Targets

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Set up a Rust-to-WebAssembly toolchain using `wasm-pack` and the `wasm32-unknown-unknown` target, understanding the build pipeline from Rust source to `.wasm` binary
- [ ] Use `wasm-bindgen` to expose Rust functions to JavaScript and call JavaScript functions from Rust, understanding how the binding layer handles type conversions
- [ ] Handle data types across the WASM boundary: numbers pass directly, strings require allocation/copying, and complex types need serialization (via `serde-wasm-bindgen` or `JsValue`)
- [ ] Build and deploy a WASM module to a browser environment using `wasm-pack build --target web` and load it from an HTML page with JavaScript
- [ ] Understand WASM limitations (no direct DOM access, no threads in basic WASM, linear memory model) and how `web-sys` and `js-sys` crates bridge the gap -- compare with Go's WASM support which bundles the entire Go runtime

## Exercises
- [ ] Use `wasm-pack new` to scaffold a project, then write a Rust function annotated with `#[wasm_bindgen]` that takes two numbers and returns their GCD using Euclid's algorithm -- build it with `wasm-pack build --target web` and call it from a JavaScript console
- [ ] Create a WASM module that exposes a `Markdown` struct with a `new(input: &str)` constructor and a `to_html(&self) -> String` method that converts simple markdown (headers, bold, italics) to HTML -- demonstrate string passing across the WASM boundary by calling it from JS
- [ ] Build a small interactive web page: write a Rust WASM module that implements a Caesar cipher (encrypt/decrypt), create an HTML page with input fields and buttons, and use JavaScript to call the WASM functions and display results -- serve locally with a simple HTTP server
- [ ] Write a Rust function that takes a `Vec<u32>` (passed via `wasm-bindgen` as a `JsValue` using serde), sorts it, and returns the sorted vector -- benchmark in the browser console against a native JavaScript sort on an array of 100,000 elements to see WASM performance characteristics

## Notes
_**SUPERSEDED**: This lesson has been split into [Lesson 92a](task-092a.md) and [Lesson 92b](task-092b.md). Use those files instead._

_Lesson not yet started._
