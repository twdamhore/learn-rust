# Lesson 049a: Lifetime Practice Part A: Diagnosing Lifetime Errors

## Section 10: Lifetimes

## Status: pending

## Added
- Split from original lesson 049 (v7 pacing review)

## Objectives
- [ ] Diagnose common lifetime error patterns by reading compiler messages carefully: "borrowed value does not live long enough", "lifetime mismatch", "cannot infer an appropriate lifetime", and "returns a reference to data owned by the current function"
- [ ] Develop strategies for fixing lifetime errors: extend the scope of the borrowed data, restructure code to avoid the borrow, return owned data instead of a reference, or use `clone()` as a deliberate trade-off
- [ ] Practice reading complex lifetime error messages from the compiler and translating them into actionable fixes
- [ ] Build intuition for when references are the right tool and when owned data (`String` instead of `&str`, `Vec<T>` instead of `&[T]`) simplifies the design without meaningful performance cost

## Exercises
- [ ] **Lifetime puzzle set (3 broken programs)**: Fix each of these programs that fail to compile due to lifetime issues: (1) a function returning `&str` that was created inside the function, (2) a struct holding `&str` that outlives the source `String`, (3) a method returning a reference where the borrow checker cannot determine the lifetime
- [ ] **Borrowed-to-owned refactor**: Take a `Tokenizer<'a>` struct that borrows a `&'a str` source and produces `Token<'a>` values (also borrowing). Refactor it to an owned `Tokenizer` that takes `String` and produces `Token` values with `String` fields. Compare the API complexity and discuss when each approach is preferable

  > **Time-box**: Aim for ~30 minutes on this exercise. If you get stuck on the refactor, focus on explaining *why* the borrow checker rejects specific patterns rather than completing the full refactor.
  >
  > **Starter code:**
  > ```rust
  > struct Tokenizer<'a> {
  >     input: &'a str,
  >     pos: usize,
  > }
  >
  > struct Token<'a> {
  >     text: &'a str,
  >     kind: TokenKind,
  > }
  >
  > enum TokenKind { Word, Number, Whitespace }
  >
  > impl<'a> Tokenizer<'a> {
  >     fn new(input: &'a str) -> Self { Tokenizer { input, pos: 0 } }
  >     fn next_token(&mut self) -> Option<Token<'a>> { todo!() }
  > }
  > ```

## Notes
_Lesson not yet started._
