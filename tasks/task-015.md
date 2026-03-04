# Lesson 015: Borrowing rules, the borrow checker, common errors

## Section 3: Ownership System

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Understand the two borrowing rules: (1) you can have any number of shared references `&T` OR exactly one mutable reference `&mut T` at a time, (2) references must always be valid (no dangling references)
- [ ] Read and interpret borrow checker error messages - understand "cannot borrow `x` as mutable because it is also borrowed as immutable" and "cannot borrow `x` as mutable more than once"
- [ ] Understand Non-Lexical Lifetimes (NLL) in practice - the compiler tracks the actual usage range of references, not lexical scope, making many previously-rejected programs valid
- [ ] Know common borrow checker patterns and fixes: introducing new scopes with `{}`, splitting borrows on different struct fields, using `.clone()` as an escape hatch, and reordering operations

## Exercises
- [ ] **Trigger the classic conflict**: Create a `Vec<i32>`, take a shared reference to an element (`let first = &v[0]`), then push to the vec (`v.push(6)`), then try to use `first` - read the error. Explain in comments why this is unsafe (the push might reallocate the Vec's buffer, invalidating the reference). Fix it by using `first` before the push
- [ ] **Fix broken code**: Debug and fix these borrow checker errors (write each as a separate function): (1) a function that tries to return a reference to a local variable, (2) a function that takes `v: &mut Vec<i32>`, gets a mutable reference to the first element (`let first = &mut v[0]`), then tries to `v.push(42)` while `first` is still alive. The conflict: `push` needs `&mut v`, but `first` already borrows part of `v` — two `&mut` accesses to the same Vec cannot coexist., (3) try to modify a `Vec<i32>` while iterating: write a loop that iterates over the vector and tries to push new elements during iteration
- [ ] **Multiple mutable borrows**: Write code that tries to create two `&mut` references to the same String simultaneously. Fix it two ways: (1) use the first `&mut` before creating the second (NLL), (2) restructure to not need two mutable borrows
- [ ] **Split borrows on tuples and variables**: Create two `String` variables. Write a function that takes mutable references to both and tries to append the contents of one to the other. See the borrow checker error when you try to pass `&mut a` and `&a` to the same function call. Fix it by: (1) cloning the source string first, (2) reading the needed value into a local variable before the mutable borrow. Explain in comments why each fix resolves the borrow conflict

## Notes
_Lesson not yet started._
