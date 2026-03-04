# Lesson 048: Struct lifetimes, 'static, lifetime bounds on generics

## Section 10: Lifetimes

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Add lifetime parameters to structs that hold references (`struct Excerpt<'a> { part: &'a str }`) and understand that the struct cannot outlive the data it borrows
- [ ] Understand the `'static` lifetime: references that live for the entire program duration (string literals, leaked allocations), and know when `'static` is required vs when it appears in trait bounds
- [ ] Use lifetime bounds on generic type parameters (`T: 'a` meaning "all references in T must live at least as long as `'a`") and understand how this constrains the types that can be used
- [ ] Understand lifetime relationships in nested structs: when one struct holds a reference to data owned by another, the lifetimes must be correctly threaded through
- [ ] Make informed decisions about when to use references in structs (borrows data, needs lifetime, more efficient) vs owned data (simpler API, no lifetime annotations, struct is self-contained)

## Exercises
- [ ] **Struct borrowing a string**: Create `struct ImportantExcerpt<'a> { part: &'a str }` and implement methods on it. Write code where the excerpt outlives the source string and observe the compiler error. Fix it by adjusting scopes
- [ ] **"Does not live long enough" debugging**: Write 2 variations of code that produce "does not live long enough" errors -- (a) struct outlives borrowed local variable, (b) returning a struct that borrows a local. Fix each one
- [ ] **'static exploration**: Verify that string literals have `'static` lifetime by assigning one to `let s: &'static str = "hello"`. Then try to assign a `String`'s borrow to `&'static str` and read the error. Discuss when `T: 'static` means "contains no non-static references" (not "lives forever"). Write a function `fn requires_static<T: 'static>(val: T) { println!("got it"); }` and show that `String` satisfies the bound (it owns its data), while `&'a str` with a non-static lifetime does not
- [ ] **Exercise 4 - Owned vs borrowed design** (~15-20 minutes -- focus on the implementation differences rather than an exhaustive comparison): Create two versions of a `Config` struct -- one with `name: &'a str` (borrowed) and one with `name: String` (owned). Implement a `parse()` function for each that constructs a `Config` from a string. Compare the API ergonomics, lifetime complexity, and performance implications. Discuss when each is appropriate

## Notes
_Lesson not yet started._
