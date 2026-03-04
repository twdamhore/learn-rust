# Lesson 067b: Advanced Async - Part B: Pin, Unpin, and Executor Internals

## Section 14: Async Rust

## Status: pending

## Added
- Split from lesson 067 (v6 pacing review)
- Pin content from original lesson 057 consolidated here where it has proper async context

## Objectives
- [ ] Understand why `Pin` exists (self-referential futures created by `async fn` with references across `.await` points)
- [ ] Understand `Pin<&mut T>` vs `Pin<Box<T>>` and when to use each
- [ ] Know which types are `Unpin` and what it means -- most standard types are `Unpin`; async fn futures are `!Unpin`
- [ ] Build a minimal single-threaded executor (stretch goal)

## Mental Model for Pin

Think of `Pin<&mut T>` like pinning a document to a specific desk. While pinned, you can read and modify the document's *contents*, but you cannot pick it up and move it to another desk. In Rust terms: you can access `&mut T` methods, but you cannot call `std::mem::swap` or `std::mem::replace` to move the value. This matters because some futures contain self-references (pointers to their own fields) -- moving them would invalidate those internal pointers. `Unpin` is the opt-out: types that are `Unpin` (most types) are safe to move even when pinned, because they contain no self-references.

## Exercises
- [ ] **Self-referential struct attempt**: Create a self-referential struct attempt and see why it fails; then explore how `Pin` prevents moving pinned values, understanding why this matters for async futures

  Try creating this struct and observe the compiler error:
  ```rust
  struct SelfRef {
      data: String,
      // This won't work — slice would need to reference data
      slice: &str,  // What lifetime goes here?
  }
  ```
  You'll find that Rust cannot express a struct where one field borrows from another field. This is exactly the problem that `Pin` solves for async futures (which are compiler-generated structs that may reference their own fields across `.await` points).

  Then explore how `Pin` prevents moving a value after it has been pinned, using `Box::pin()` and `Pin::as_mut()`.
- [ ] **Simple block_on**: Implement a simple `block_on` function that polls a future in a loop with a basic `Waker` (using `std::task::Wake` or `RawWaker`); test with the futures from lesson 067a

  > **Important**: This exercise uses `unsafe` code (covered in lesson 073) to construct a `Waker`. The unsafe scaffold is provided for you — **do not modify the unsafe code**. Focus entirely on the `block_on` polling loop logic. You'll understand the unsafe parts when you reach lesson 073.

  **Provided scaffold** -- Use this provided waker implementation. Your job is to write the `block_on` function that uses it.

  ```rust
  use std::task::{RawWaker, RawWakerVTable, Waker};

  // Minimal no-op waker — wakes by doing nothing (suitable for block_on that polls in a loop)
  fn dummy_raw_waker() -> RawWaker {
      fn no_op(_: *const ()) {}
      fn clone(data: *const ()) -> RawWaker {
          RawWaker::new(data, &VTABLE)
      }
      const VTABLE: RawWakerVTable = RawWakerVTable::new(clone, no_op, no_op, no_op);
      RawWaker::new(std::ptr::null(), &VTABLE)
  }

  fn dummy_waker() -> Waker {
      // SAFETY: RawWaker follows the contract — clone returns a valid RawWaker,
      // wake/wake_by_ref/drop are no-ops which is safe.
      unsafe { Waker::from_raw(dummy_raw_waker()) }
  }
  ```
- [ ] **(Stretch) Task queue executor**: Extend `block_on` to support spawning multiple tasks with a simple task queue; poll tasks round-robin until all complete

## Notes
_Lesson not yet started._
