# Lesson 041: Trait bounds, where clauses, impl Trait syntax

## Section 9: Generics & Traits

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Use trait bounds on generic functions to constrain type parameters (`fn print_it<T: Display>(item: T)`) and understand that bounds tell the compiler what capabilities a type must have
- [ ] Refactor inline trait bounds to `where` clauses for readability, especially when there are multiple type parameters or complex bounds (`fn foo<T, U>(t: T, u: U) where T: Display + Clone, U: Debug`)
- [ ] Use `impl Trait` in argument position as syntactic sugar for generic bounds (`fn print_it(item: impl Display)`) and understand that it is equivalent to the generic form for function arguments
- [ ] Combine multiple trait bounds with `+` syntax (e.g., `T: Display + Clone + PartialOrd`) and understand that each bound further constrains which types are accepted
- [ ] Understand `Sized` as an implicit default bound on all generic types, and use `?Sized` to opt out when you want to accept dynamically-sized types like `str` or `[T]`

## Exercises
- [ ] **Exercise 1 - Bounded print function**: Write a function `fn print_labeled<T: Display + Clone>(label: &str, item: T)` that prints a label and the item, then returns a clone of the item. Test with `String`, `i32`, and a custom struct that derives both traits
- [ ] **Exercise 2 - Where clause refactoring**: Start with a function signature that has 3 type parameters with inline bounds (making the signature hard to read), then refactor it to use a `where` clause. Verify both versions compile identically
- [ ] **Exercise 3 - impl Trait parameter**: Write a function `fn summarize_all(items: &[impl Summary])` that calls `summarize()` on each item in a slice. Compare this with the explicit generic form `fn summarize_all<T: Summary>(items: &[T])` and note that `impl Trait` in argument position means all items must be the same concrete type
- [ ] **Exercise 4 - ?Sized exploration**: Write a function `fn print_ref<T: Display + ?Sized>(item: &T)` that can accept both `&String` and `&str`. Then try removing `?Sized` and observe which calls no longer compile, understanding why `Sized` matters

## Notes
_Lesson not yet started._
