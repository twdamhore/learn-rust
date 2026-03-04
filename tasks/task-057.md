# Lesson 057: Cow<T>, Weak references, Pin<T>, PhantomData

## Section 12: Smart Pointers & Interior Mutability

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Use `Cow<'a, T>` (Clone on Write) to write functions that accept both owned and borrowed data, cloning only when mutation is actually needed
- [ ] Use `Weak<T>` references (via `Rc::downgrade`) to break reference cycles and create non-owning references that don't prevent cleanup
- [ ] Understand `Pin<T>` at a conceptual level: it prevents a value from being moved in memory, which is essential for self-referential types and async futures
- [ ] Use `PhantomData<T>` to indicate that a struct logically owns or relates to a type `T` even though it doesn't physically contain one, affecting drop checking and variance

## Exercises
- [ ] **Cow for flexible APIs**: Write a function `normalize_name(name: &str) -> Cow<str>` that returns the input unchanged (borrowed) if it's already trimmed and lowercase, or returns a newly allocated trimmed-and-lowered version (owned) if modification is needed. Benchmark-style test: call it with already-normalized strings and verify no allocation occurs (check `Cow::is_borrowed()`).
- [ ] **Breaking cycles with Weak**: Revisit the reference cycle from lesson 055. Replace one of the `Rc` links with a `Weak<T>` reference. Use `Weak::upgrade()` to access the data (returns `Option<Rc<T>>`). Verify that `strong_count()` now drops to zero and memory is properly freed when the owning `Rc` values are dropped.
- [ ] **Pin exploration**: Create a struct that stores a `String` and an index into it. Attempt to move the struct after creation and observe the problem. Then wrap it in `Pin<Box<T>>` and demonstrate that `Pin` prevents moves. Explain in comments why this matters for `async`/`await` (futures are self-referential).
- [ ] **PhantomData for type safety**: Create a generic `Id<T>` struct (containing just a `u64`) that uses `PhantomData<T>` to tie it to a specific entity type. Define `User` and `Product` types. Show that `Id<User>` and `Id<Product>` are different types at compile time -- you cannot accidentally pass an `Id<User>` where an `Id<Product>` is expected.

## Notes
_**SUPERSEDED**: This lesson has been split into [Lesson 57a](task-057a.md) and [Lesson 57b](task-057b.md). Use those files instead._

_Lesson not yet started._
