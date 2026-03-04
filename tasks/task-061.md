# Lesson 061: Send and Sync traits, thread safety guarantees

## Section 13: Concurrency

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Understand the `Send` marker trait: a type is `Send` if it can be safely transferred (moved) to another thread
- [ ] Understand the `Sync` marker trait: a type is `Sync` if a shared reference `&T` can be safely shared between threads (i.e., `T: Sync` means `&T: Send`)
- [ ] Know which standard library types are `Send`/`Sync` and which are not: `Rc` is `!Send` and `!Sync`, `RefCell` is `!Sync`, raw pointers are `!Send` and `!Sync`, `Arc` and `Mutex` are both `Send` and `Sync`
- [ ] Use `Send + Sync` bounds in generic functions and trait objects to require thread safety
- [ ] Understand that `Send` and `Sync` are auto-traits: the compiler derives them automatically for your types based on their fields, and you rarely need to implement them manually

## Exercises
- [ ] **Rc is not Send**: Attempt to send an `Rc<i32>` to a spawned thread. Read and annotate the compiler error message. Replace `Rc` with `Arc` and verify it compiles. Explain in comments why `Rc`'s non-atomic reference count makes it unsafe to share across threads.
- [ ] **Sync exploration**: Create a struct containing a `Cell<i32>` field. Try to share a reference to it across threads (e.g., using `std::thread::scope`). Observe the `!Sync` error. Replace `Cell` with `AtomicI32` and verify it works. Explain the relationship between `Sync` and `&T: Send`.

  > **Note:** `AtomicI32` is covered in the next lesson (062). For now, just know it's an integer that can be safely shared between threads without a lock. Alternatively, you could fix this with `Arc<Mutex<i32>>` using knowledge from lesson 060.
- [ ] **Custom struct analysis**: Create several structs with different field combinations: (a) all `Send + Sync` fields, (b) one `Rc` field, (c) one `RefCell` field, (d) one raw pointer field. Write a compile-time assertion function `fn assert_send<T: Send>() {}` and `fn assert_sync<T: Sync>() {}` and call them for each struct. Document which pass and which fail, and why.
- [ ] **Thread-safe trait object**: Define a trait `Task` with `fn execute(&self)`. Write a function `run_tasks(tasks: Vec<Box<dyn Task + Send + Sync>>)` that spawns a thread for each task. Implement `Task` for a struct with `Arc<Mutex<Vec<String>>>` logging. Demonstrate that removing the `Send` bound causes a compile error when spawning threads.

## Notes
_Lesson not yet started._
