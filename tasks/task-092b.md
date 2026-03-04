# Lesson 092b: WebAssembly - Part B: Browser Integration

## Section 20: Special Targets

## Status: pending

## Prerequisites
- Lesson 092a (Rust to WASM Basics)
- Basic HTML/JavaScript familiarity (creating an HTML file, using `<script>` tags, calling functions from JS)

## Added
- Split from lesson 092 (v6 pacing review)

## Objectives
- [ ] Use `wasm-bindgen` to interact with browser APIs: understand how `#[wasm_bindgen]` exposes Rust functions to JavaScript and how the generated JS glue code handles type conversions
- [ ] Load a WASM module from JavaScript in a browser: serve files with a local HTTP server, use `import init` from the generated JS module, and call Rust functions from JS
- [ ] Pass data between JavaScript and Rust: numbers pass directly, strings require allocation/copying, and understand the basics of the WASM linear memory model

## Exercises
- [ ] **Exercise 1 -- Load WASM in browser**: Create an HTML page that loads the WASM module built in lesson 092a. Use JavaScript to call the GCD and slugify functions, display the results on the page. Serve locally with `python3 -m http.server` or similar.
- [ ] **Exercise 2 -- Interactive text transformer**: Build a simple interactive tool: write a Rust WASM module with 2-3 text transformation functions (e.g., uppercase, reverse, ROT13). Create a basic HTML page with an input field and buttons that call each WASM function and display the result. Keep the HTML/JS minimal -- the focus is on the Rust-to-JS bridge, not web design.

## Notes

> **Starter HTML template**:
> ```html
> <!DOCTYPE html>
> <html>
> <head><meta charset="utf-8"><title>WASM Demo</title></head>
> <body>
>   <script type="module">
>     import init, { /* your exported functions here */ } from './pkg/lesson_092.js';
>     async function run() {
>       await init();
>       // Call your WASM functions here
>     }
>     run();
>   </script>
> </body>
> </html>
> ```
> Serve with `python3 -m http.server` and open `http://localhost:8000` in your browser.

_Lesson not yet started._
_Split from original lesson 092 which covered WASM basics through browser integration (~2.5-3.5 hr estimated). This part focuses on browser integration with simplified exercises._
_Exercises requiring deep JavaScript/HTML knowledge have been simplified from the original lesson. The markdown parser and Caesar cipher interactive page from the original have been replaced with simpler alternatives._
