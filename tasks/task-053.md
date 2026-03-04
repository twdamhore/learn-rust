# Lesson 053: Higher-Ranked Trait Bounds

## Section 10: Lifetimes

## Status: pending

## Added
- Split from original lesson 053 (v6 pacing review)

## Objectives
- [ ] Understand what Higher-Rank Trait Bounds (HRTBs) are and the `for<'a>` syntax: a way to say "this function/closure works for any lifetime", not just one specific lifetime chosen by the caller
- [ ] Recognize where HRTBs appear in the standard library (e.g., `Fn` traits, `Iterator::for_each`, `str::parse` requiring `FromStr`) and why they are necessary in those contexts
- [ ] Write functions that accept closures working with references using `for<'a>` bounds, understanding why a regular lifetime parameter `'a` on the outer function is insufficient
- [ ] Understand why HRTBs are needed vs regular lifetime parameters: regular parameters fix a single lifetime at the call site, while HRTBs allow the closure to work with references of any lifetime inside the function body

---

**When will you encounter HRTBs?** In practice, you rarely write `for<'a>` yourself. You'll encounter it when:
- Using closures that accept references (e.g., `F: for<'a> Fn(&'a str) -> &'a str`)
- Working with the `Fn` trait family (they use HRTBs internally)
- Reading library APIs that accept callbacks operating on borrowed data
- Understanding compiler error messages that mention `for<'a>`

This lesson is about recognition and understanding, not daily usage.

---

> **Closure crash course** (formally covered in lesson 055): Closures are Rust's anonymous functions, written as `|arg| expression` or `|arg| { body }`. They capture variables from their environment. Rust has three closure traits:
> - `Fn` — borrows captured variables (can be called multiple times)
> - `FnMut` — mutably borrows captured variables
> - `FnOnce` — takes ownership of captured variables (can only be called once)
>
> For this lesson, you just need to know the syntax `|x| x + 1` and that `Fn(&str) -> &str` means "a closure that borrows a `&str` and returns a `&str`". Full coverage comes in lesson 055.

## Exercises
- [ ] **HRTB with closures**: Write a function `fn apply_to_ref<F>(f: F, data: &[String]) where F: for<'a> Fn(&'a str) -> &'a str` that applies `f` to each string in the slice and collects results. First attempt without `for<'a>` (using `F: Fn(&str) -> &str`) and observe how the compiler desugars it. Then add the explicit HRTB and verify it compiles. Test with a closure that returns a substring slice.
- [ ] **Custom trait method with HRTBs**: Study how `Iterator::for_each` uses HRTBs internally. Then implement the `Processor` trait below for the `TextBatch` struct so that `process` applies the closure to each string in `items`.

  ```rust
  // Starter code — implement this trait for TextBatch:
  trait Processor {
      fn process<F>(&self, f: F)
      where
          F: for<'a> Fn(&'a str);
  }

  struct TextBatch {
      items: Vec<String>,
  }
  ```
  Your task: implement `Processor` for `TextBatch` so that `process` applies the closure to each string in `items`.
- [ ] **(Optional) HRTB scavenger hunt**: Find 3 examples of `for<'a>` in the standard library documentation (hint: look at `Fn` trait definitions, `str` methods, iterator adaptors). For each, write a comment explaining why the HRTB is necessary and what would go wrong without it.

## Notes
_Lesson not yet started._
