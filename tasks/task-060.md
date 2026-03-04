# Lesson 060: RefCell<T>, Cell<T> - interior mutability, runtime borrow checking

## Section 12: Smart Pointers & Interior Mutability

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Understand the interior mutability pattern: obtaining `&mut` access to data inside an immutable reference, checked at runtime instead of compile time
- [ ] Use `RefCell<T>` to borrow data mutably at runtime via `borrow()` and `borrow_mut()`, understanding that violating borrow rules causes a runtime panic (not a compile error)
- [ ] Use `Cell<T>` for simple `Copy` types where you need interior mutability without the overhead of runtime borrow tracking
- [ ] Combine `Rc<RefCell<T>>` to achieve shared mutable state in single-threaded code, the idiomatic Rust pattern for multiple owners that need mutation
- [ ] Compare interior mutability with Java's approach (all objects mutable by default, synchronized for thread safety) and understand why Rust makes this explicit

## Exercises
- [ ] **RefCell basics**: Create an `Rc<RefCell<Vec<String>>>` shared between two structs. Have each struct push items into the shared vec through its `Rc` reference. Print the final contents from both handles to verify shared mutation works.
- [ ] **Runtime borrow panic**: Write code that deliberately creates two `borrow_mut()` calls on the same `RefCell` simultaneously (e.g., hold one `RefMut` while trying to get another). Catch or observe the panic. Then fix it by ensuring borrows don't overlap.
- [ ] **Observer pattern**: Define an `Observer` trait with `fn update(&mut self, msg: &str)`. Implement an `EventBus` struct that holds a `Vec<Box<dyn Observer>>`. Add a `notify(&mut self, msg: &str)` method on `EventBus` that calls `update` on each observer. Create two concrete observers (e.g., `Logger` and `Counter`), register them with the `EventBus`, send a notification, and print each observer's state. (Note: `Rc<RefCell<>>` is already demonstrated in Exercises 1-2; this exercise focuses on trait objects with `Box<dyn Observer>`.)
- [ ] **Cell for counters**: Create a struct with a `Cell<u32>` field that acts as an invocation counter. Implement a method `&self` (not `&mut self`) that increments the counter each time it's called. Demonstrate that this works even through shared references, and explain when `Cell` is preferred over `RefCell`.

## Notes
_Lesson not yet started._
