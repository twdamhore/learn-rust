# Lesson 061: Smart Pointers Part A - Cow and Weak References

## Section 12: Smart Pointers & Interior Mutability

## Status: pending

## Added
- Split from original lesson 061 (overloaded ~2+ hrs)

## Objectives
- [ ] Use `Cow<'a, T>` (Clone on Write) to write functions that accept both owned and borrowed data, cloning only when mutation is actually needed
- [ ] Understand when `Cow` avoids unnecessary allocations: the borrowed variant is used when no modification is needed, and the owned variant is produced only on first write
- [ ] Compare `Cow` to Java's `String` (always owned, immutable but freely copied by GC) and Go's implicit copy-on-write slice behavior -- Rust makes the optimization explicit
- [ ] Use `Weak<T>` references (via `Rc::downgrade`) to break reference cycles and create non-owning references that don't prevent cleanup
- [ ] Understand the relationship between `Rc::strong_count()` and `Rc::weak_count()` -- data is freed when strong count reaches zero, weak references become invalid at that point
- [ ] Use `Weak::upgrade()` to safely attempt access to data that may have been freed (returns `Option<Rc<T>>`)

## Exercises
- [ ] **Cow for flexible APIs**: Write a function `normalize_name(name: &str) -> Cow<str>` that returns the input unchanged (borrowed) if it's already trimmed and lowercase, or returns a newly allocated trimmed-and-lowered version (owned) if modification is needed. Test with already-normalized strings and verify no allocation occurs (check `Cow::Borrowed` via pattern matching or `matches!` macro). Test with strings that need modification and verify `Cow::Owned` is returned.
- [ ] **Cow in a config parser**: Write a function `resolve_env(value: &str) -> Cow<str>` that checks if a config value contains `${VAR_NAME}` placeholders. If no placeholders are found, return the input borrowed. If placeholders exist, return a new string with them replaced by environment variable values (or a default). Demonstrate that config values without placeholders avoid allocation entirely.
- [ ] **Breaking cycles with Weak**: Revisit the reference cycle from lesson 059. Replace one of the `Rc` links with a `Weak<T>` reference. Use `Weak::upgrade()` to access the data (returns `Option<Rc<T>>`). Verify that `strong_count()` now drops to zero and memory is properly freed when the owning `Rc` values are dropped.
- [ ] **Tree with parent back-references [STRETCH]**: Build a tree structure where each node owns its children via `Vec<Rc<RefCell<Node>>>` but has an optional back-reference to its parent via `Weak<RefCell<Node>>`. Create a tree with a root and two children. Navigate from a child to its parent using `upgrade()`. Drop the root and verify that children's parent `Weak` references now return `None` from `upgrade()`.

## Notes
_Lesson not yet started._
