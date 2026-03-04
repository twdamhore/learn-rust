# Lesson 014: References and borrowing - & and &mut

## Section 3: Ownership System

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Create shared (immutable) references with `&T` - understand that references borrow a value without taking ownership, allowing the original owner to keep using it
- [ ] Create mutable references with `&mut T` - understand that mutable references allow modification of the borrowed value and require the original binding to be `mut`
- [ ] Understand references as non-owning pointers: they point to data owned by someone else, the data cannot be dropped while a reference exists, and references always point to valid data (no null references)
- [ ] Pass references to functions - understand `fn calculate_length(s: &String) -> usize` vs taking ownership, and why `&str` is usually preferred over `&String` in function parameters
- [ ] Understand reference scope informally - a reference is valid from where it's created to where it's last used (Non-Lexical Lifetimes), not necessarily to the end of the block

## Exercises
- [ ] **References instead of moves**: Take the `take_ownership` function from lesson 012 and rewrite it as `fn calculate_length(s: &String) -> usize` - verify the caller can still use the String after the call. Then change the parameter to `&str` and observe that it still works with `&my_string`
- [ ] **Mutable references**: Write a function `fn append_greeting(s: &mut String)` that pushes " hello!" onto the string. Call it and verify the original String is modified. Then write `fn push_value(v: &mut Vec<i32>, val: i32)` and use it to modify a vector
- [ ] **Java/Go comparison**: Write (in comments) the Java equivalent of passing an ArrayList to a method that modifies it, and the Go equivalent using a pointer receiver. Then write the Rust version using `&mut`. Annotate the key difference: Rust makes mutability explicit at both the call site and function signature
- [ ] **Reference scope experiment**: Create a `String`, take a shared reference, use the reference, then take a mutable reference after the shared one's last use - verify this compiles (NLL). Then move the shared reference's usage after the mutable reference and observe the error. Add comments explaining NLL

## Notes
_Lesson not yet started._
