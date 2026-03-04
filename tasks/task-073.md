# Lesson 073: Unsafe blocks, raw pointers, dereferencing

## Section 16: Unsafe & FFI

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Understand the five things `unsafe` unlocks: dereference raw pointers, call unsafe functions, access mutable statics, implement unsafe traits, access union fields
- [ ] Create raw pointers (`*const T` and `*mut T`) from references and understand that creating them is safe but dereferencing is unsafe
- [ ] Understand the difference between `unsafe {}` blocks (caller asserts invariants) and `unsafe fn` (caller must uphold invariants)
- [ ] Know when `unsafe` is genuinely needed vs when there is a safe alternative
- [ ] Understand the safety contract: `unsafe` does not turn off the borrow checker -- it only permits the five specific operations

## Exercises
- [ ] **Raw pointer basics**: Create `*const i32` and `*mut i32` from references using `as` casts; dereference them inside `unsafe` blocks; modify the value through the mutable raw pointer and verify the change
- [ ] **Reference round-trip**: Convert a `&mut Vec<i32>` to a `*mut Vec<i32>`, then back to `&mut Vec<i32>` inside an `unsafe` block; push an element through the reconstituted reference and verify the vec was modified
- [ ] **Mutable static**: Declare a `static mut COUNTER: u32 = 0`; write an unsafe function `increment_counter()` that increments it; call it from `main` inside an `unsafe` block and print the result; add a comment explaining why mutable statics are unsafe (data races in multithreaded code)
- [ ] **Safe vs unsafe quiz**: Write 8 operations as comments (e.g., "index a slice with `[]`", "call `slice::get_unchecked`", "cast `&T` to `*const T`", "dereference `*const T`") and annotate each as safe or unsafe with an explanation; verify by writing the code and seeing which ones require `unsafe`

## Notes
_Lesson not yet started._
