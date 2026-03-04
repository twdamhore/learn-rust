# Lesson 054: Box<T> - heap allocation, recursive types

## Section 12: Smart Pointers & Interior Mutability

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Understand that `Box<T>` allocates data on the heap and owns it, with automatic cleanup via the `Drop` trait when the `Box` goes out of scope
- [ ] Create recursive data types (linked lists, trees) using `Box<T>` to give them a known size at compile time
- [ ] Understand `Box<T>` as a smart pointer that implements `Deref` (auto-dereferencing to `&T`) and `Drop` (automatic heap cleanup)
- [ ] Use `Box<dyn Trait>` for dynamic dispatch when you need to store different concrete types behind a common trait interface
- [ ] Compare `Box<T>` with Java's `new` (everything is heap-allocated in Java) and Go's pointer semantics, understanding that Rust makes heap allocation explicit

## Exercises
- [ ] **Singly linked list**: Implement `enum List { Cons(i32, Box<List>), Nil }` with methods `push_front`, `to_vec`, and `len`. Create a list `3 -> 2 -> 1 -> Nil` and verify its contents. Explain why `Box` is required here (what error do you get without it?).
- [ ] **Binary tree [STRETCH]**: Define `enum Tree<T> { Leaf, Node { value: T, left: Box<Tree<T>>, right: Box<Tree<T>> } }`. Implement `insert` for a binary search tree, `contains` to search, and [OPTIONAL within STRETCH] implement `in_order` traversal to return a sorted `Vec<T>` if time permits. Test with integers.
- [ ] **Box for large values**: Create a large struct (e.g., `[u8; 1_000_000]`) and demonstrate boxing it to avoid stack overflow. Use `std::mem::size_of_val` to show the size of a `Box<T>` is always pointer-sized regardless of `T`.
- [ ] **Box<dyn Trait> dispatch**: Define a `Logger` trait with `log(&self, message: &str)` and `level(&self) -> &str` methods. Implement it for `ConsoleLogger`, `FileLogger`, and `JsonLogger`. Create a `Vec<Box<dyn Logger>>` containing all three and iterate to log a test message with each, printing the logger's level. Compare this with Java interfaces and Go interfaces.

## Notes
_Lesson not yet started._
