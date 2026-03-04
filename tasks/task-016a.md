# Lesson 016a: Thinking in Ownership - Part A: Ownership Patterns and Strategies

## Section 3: Ownership System

## Status: pending

## Added
- Split from task-016 [NEW - bridging lesson] due to overloaded pacing (~3-4 hr)
- Part A focuses on concepts and simple ownership exercises using only lessons 001-015 concepts (~1.5 hr)

## Objectives
- [ ] Choose between clone, borrow, and move for any given situation -- understand the tradeoffs of each strategy and when each is appropriate
- [ ] Recognize when to restructure code to satisfy the borrow checker -- instead of fighting the compiler, use its errors as design feedback
- [ ] Apply common ownership refactoring strategies: split structs into smaller pieces, return owned values instead of references to locals, use indices instead of references into collections, reorder operations to shorten borrow lifetimes

## Exercises
- [ ] **Fix 3 broken programs**: Fix each of these 3 ownership-broken programs (each is a separate small function): (1) a function that tries to return `&str` referencing a local `String` (fix the dangling reference), (2) a loop that moves a `Vec` into a function on each iteration (fix the use-after-move), (3) a function that takes `String` as parameter when `&str` would suffice (improve the API). Fix each using only the ownership strategies you know: clone, borrow, or restructure.
- [ ] **Refactor mutate-while-iterating**: Write a function that tries to mutate a `Vec<i32>` while iterating over it (e.g., doubling values that meet a condition), fix it by collecting indices first, then mutating. Observe how the borrow checker prevents the original approach and why the index-based solution works.
- [ ] **Compare 3 approaches to a shared-data problem**: Given a function that needs to use the same `String` in two places, implement three solutions: (1) clone everything, (2) use references/borrows, (3) restructure to avoid the conflict entirely. Add a comment to each explaining the tradeoff (simplicity vs performance vs readability).

## Notes
- This lesson uses ONLY concepts from lessons 001-015: variables, types, functions, control flow, ownership, moves, references, borrowing rules.
- No structs, no impl blocks, no Option, no iterators beyond basic `for` loops.
- If you get stuck on a borrow checker error, read the compiler message carefully -- it is telling you exactly what went wrong.
_Lesson not yet started._
