# Lesson 056: move closures, closures as parameters and return values

## Section 11: Closures & Functional Patterns

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Use the `move` keyword with closures to force ownership transfer of captured variables, even when the closure body only needs a reference
- [ ] Pass closures as function parameters using both generic bounds (`impl Fn`, `where F: Fn`) and trait objects (`&dyn Fn`, `Box<dyn Fn>`)
- [ ] Return closures from functions using `impl Fn(...)` syntax, understanding why the concrete type cannot be named
- [ ] Store closures in structs and collections using `Box<dyn Fn>` for heterogeneous closure storage
- [ ] Compare `move` closure semantics with Java's effectively-final lambda restriction and Go's closure-over-variable behavior

## Exercises
- [ ] **Move closures — returning closures that capture locals**: Write a function `make_greeting(name: String) -> impl Fn() -> String` that captures `name` by moving it into the closure and returns a greeting string. Call it, then try to use `name` after passing it to the function and observe the move error. Compare: in Go, the closure would capture a reference to `name` and both could still use it — in Rust, ownership is transferred
- [ ] **Returning closures**: Write a function `make_scaler(factor: f64) -> impl Fn(f64) -> f64` that returns a closure scaling its argument by `factor`. Then write `make_greeter(name: String) -> impl Fn() -> String` that returns the captured name in a greeting. Explain why `move` is needed in the second case.
- [ ] **Callback system [STRETCH]**: Build a simple `EventEmitter` struct that stores a `Vec<Box<dyn Fn(&str)>>` of listener callbacks. Implement `on(&mut self, callback: impl Fn(&str) + 'static)` to register listeners and `emit(&self, event: &str)` to call all listeners. Test it with multiple closures that capture different data.
- [ ] **Closure trait selection**: Write three functions that each accept a different closure trait bound (`Fn`, `FnMut`, `FnOnce`) and demonstrate which closures can be passed to which. Show that an `Fn` closure can satisfy `FnMut` and `FnOnce` bounds (trait hierarchy).

## Notes
_Lesson not yet started._
