# Lesson 059: Rc<T>, Arc<T> - reference counting, shared ownership

## Section 12: Smart Pointers & Interior Mutability

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Understand `Rc<T>` for single-threaded shared ownership: multiple owners of the same heap data with automatic cleanup when the last `Rc` is dropped
- [ ] Use `Rc::clone()` to create new references (cheap reference count increment, not a deep clone) and inspect counts with `Rc::strong_count()`
- [ ] Understand `Arc<T>` as the thread-safe version of `Rc<T>`, using atomic operations for reference counting at a small performance cost
- [ ] Know when to choose each: `Box<T>` for single ownership, `Rc<T>` for shared ownership (single-threaded), `Arc<T>` for shared ownership (multi-threaded)
- [ ] Compare Rust's explicit reference counting with Java's garbage collector (which handles shared references invisibly) and understand the reference cycle pitfall

## Exercises
- [ ] **Shared graph nodes**: Build a simple directed acyclic graph where nodes can have multiple parents. Use `Rc<Node>` so that two parent nodes can both own a reference to the same child. Print `Rc::strong_count()` at each step to observe the reference count changes.
- [ ] **Reference cycle memory leak**: Create two nodes that each hold an `Option<Rc<Node>>` pointing to the other (using `RefCell` for interior mutability). Observe that `Rc::strong_count()` never drops to zero, demonstrating a memory leak. Explain why Rust's ownership model does not prevent this.
  > **Preview**: This exercise uses `RefCell` and `borrow_mut()` from lesson 060. The code is provided for you — focus on understanding the reference cycle concept, not the RefCell mechanics. You'll learn RefCell properly in the next lesson.

  ```rust
  // Preview: RefCell provides interior mutability (covered fully in lesson 060)
  // .borrow() returns a shared reference, .borrow_mut() returns a mutable reference
  use std::cell::RefCell;
  use std::rc::Rc;

  struct Node {
      value: i32,
      next: Option<Rc<RefCell<Node>>>,
  }

  // Create nodes
  let a = Rc::new(RefCell::new(Node { value: 1, next: None }));
  let b = Rc::new(RefCell::new(Node { value: 2, next: Some(Rc::clone(&a)) }));

  // Mutate through RefCell to create a cycle
  a.borrow_mut().next = Some(Rc::clone(&b));  // a -> b -> a (cycle!)
  ```
- [ ] **Rc clone semantics**: Create an `Rc<Vec<String>>`, clone it three times, and verify all clones point to the same data (pointer equality via `Rc::ptr_eq`). Drop clones one by one, printing `strong_count()` after each drop, and verify the data is freed only when the last `Rc` is dropped.
- [ ] **Arc for threads**: Create an `Arc<Vec<i32>>` and share it across 4 threads. Each thread reads a quarter of the vector and returns the sum. Join all threads and combine the partial sums. Verify this would fail with `Rc` (try it and read the compiler error).
  > **Preview**: This exercise uses `std::thread::spawn` from lesson 063. The thread code is provided — focus on understanding why `Arc` (not `Rc`) is needed for thread-safe shared ownership. Threads are covered properly in lesson 063.

## Notes
_Lesson not yet started._
