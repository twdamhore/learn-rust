# Lesson 012: Stack vs heap, what ownership is, move semantics

## Section 3: Ownership System

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Know the three ownership rules: (1) each value has exactly one owner, (2) there can only be one owner at a time, (3) when the owner goes out of scope the value is dropped
- [ ] See moves in action with `String` - understand that `let s2 = s1;` moves the heap-allocated String, invalidating `s1`
- [ ] Understand stack-only data (integers, bools, chars, fixed-size tuples of Copy types) vs heap data (String, Vec) and why they behave differently on assignment
- [ ] Know all the places where moves happen: variable assignment (`let s2 = s1`), passing arguments to functions, returning values from functions, and pattern matching
- [ ] Read and interpret move-related compiler errors like "value used after being moved" and "use of moved value"

## Exercises
- [ ] **Trigger a move error**: Create a `String`, assign it to a second variable, then try to print the original - read and annotate the compiler error message explaining what each part means
- [ ] **Function move**: Write a function `fn take_ownership(s: String)` that prints the string. Call it with a String variable, then try to use the variable after the call - observe the move. Then write `fn give_ownership() -> String` that creates and returns a String, and `fn take_and_give_back(s: String) -> String` that takes and returns
- [ ] **Stack vs heap**: Write a program that assigns an `i32` to a new variable and uses both (works fine), then does the same with `String` (fails). Add comments explaining why `i32` is copied while `String` is moved by drawing the stack/heap layout
- [ ] **Move in collections**: Create a `Vec<String>` with three elements. Extract one element using `let s = vec[0]` (see the error), then use `.remove(0)` or `.pop()` instead. Explain in comments why indexing doesn't move but remove/pop does

## Notes
_Lesson not yet started._
