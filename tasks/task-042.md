# Lesson 042: impl Trait in argument vs return position, when to use which

## Section 9: Generics & Traits

## Status: pending

## Added
- Initial curriculum design [NEW - bridging lesson]

## Objectives
- [ ] Understand `impl Trait` in argument position as syntactic sugar for a generic type parameter -- the caller chooses the concrete type, and the function is monomorphized for each type used
- [ ] Understand `impl Trait` in return position as an existential type -- the function chooses a single concrete type to return, but hides it from the caller. The caller only knows it implements the trait
- [ ] Know when return-position `impl Trait` is appropriate (returning iterators, closures, or complex types whose concrete name is unwieldy) and when it falls short (cannot return different concrete types from different branches)
- [ ] Understand the key limitation: return-position `impl Trait` requires all return paths to produce the same concrete type -- `if cond { vec.iter() } else { slice.iter() }` will not compile because they are different iterator types
- [ ] Compare `impl Trait` (static dispatch, one concrete type) with `dyn Trait` (dynamic dispatch, multiple concrete types) as a preview of lesson 043

## Exercises
- [ ] **Argument position equivalence**: Write the same function three ways -- (a) `fn process(item: impl Summary)`, (b) `fn process<T: Summary>(item: T)`, (c) [Preview] Write a version using `&dyn Summary` -- observe that it compiles. We'll explain how dynamic dispatch works via vtables in lesson 043. For now, just note that it looks different from `impl Summary`. Write tests calling all three
- [ ] **Return-position iterator**: Write a function `fn even_numbers(up_to: u32) -> impl Iterator<Item = u32>` that returns a chained iterator filtering even numbers. Note how without `impl Iterator`, you would need to spell out the full iterator adapter type
- [ ] **Return-position limitation**: Write a function that tries to return different iterator types from different `if/else` branches using `impl Iterator`. Read the compiler error, then fix it two ways: (a) collect into a `Vec` and return `vec.into_iter()`, (b) use `Box<dyn Iterator>` instead
- [ ] **Closure return**: Write a function `fn make_multiplier(factor: i32) -> impl Fn(i32) -> i32` that returns a closure multiplying its argument by `factor`. Explain why `impl Fn` is necessary here (closures have anonymous types that cannot be named)

## Notes
_Lesson not yet started._
