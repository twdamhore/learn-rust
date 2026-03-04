# Lesson 089: Sealed traits, marker traits, type-level programming

## Section 17: Advanced Type System

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Implement sealed traits using a private module pattern so that only types within your crate can implement the trait, preventing downstream crates from adding implementations
- [ ] Understand marker traits (`Send`, `Sync`, `Unpin`, `Sized`) -- traits with no methods that communicate properties to the compiler and to generic bounds
- [ ] Explore type-level programming basics: using types as values, encoding booleans and natural numbers at the type level, and making the compiler compute things at compile time
- [ ] Use const generics (`struct Array<T, const N: usize>`) for type-level values and understand their relationship to type-level programming

> **Callback**: You already used const generics (`<const N: usize>`) in lesson 082's SafeBuffer exercise. This lesson covers them properly — the rules, limitations, and advanced patterns.
- [ ] Recognize when these advanced patterns are worth the complexity vs when simpler runtime checks suffice

## Exercises
- [ ] **Exercise 1 -- Sealed trait**: Create a `trait Primitive: private::Sealed {}` with a private `mod private { pub trait Sealed {} }`. Implement `Sealed` and `Primitive` for `i32`, `f64`, `bool`, and `String`. Write a generic function `fn describe<T: Primitive>(val: &T)` and verify that users outside your module cannot implement `Primitive` for their own types.
- [ ] **Exercise 2 -- Custom marker trait**: Define an `unsafe trait ThreadSafeCache {}` marker trait (no methods). Implement it for specific cache types. Write a function `fn use_cache<C: ThreadSafeCache>(cache: &C)` that only accepts types explicitly marked as thread-safe. Discuss why it is `unsafe` to implement (the implementor is asserting a guarantee the compiler cannot verify).
- [ ] **Exercise 3 -- PhantomData type-level tags**: _Building on the `PhantomData` tagged types from lesson 087 Exercise 4..._ Build a `Permission<Level>` system where `Level` is one of `struct ReadOnly;`, `struct ReadWrite;`, `struct Admin;`. Use `PhantomData<Level>` to carry the permission at the type level. Write functions that require specific permission levels. Implement a `fn elevate(perm: Permission<ReadOnly>) -> Permission<ReadWrite>` function and verify that you cannot elevate `ReadWrite` to `Admin` without an explicit function.
- [ ] **Exercise 4 [STRETCH] -- Const generics**: Create a `Matrix<T, const ROWS: usize, const COLS: usize>` struct backed by `[[T; COLS]; ROWS]`. Implement `multiply` so that `Matrix<f64, M, N> * Matrix<f64, N, P>` produces `Matrix<f64, M, P>` -- the compiler should reject dimension mismatches. Implement `transpose` returning `Matrix<T, COLS, ROWS>`.

  **Scaffold — impl Mul with triple const generics:**
  ```rust
  use std::ops::Mul;

  struct Matrix<T, const ROWS: usize, const COLS: usize> {
      data: [[T; COLS]; ROWS],
  }

  // Matrix<M,N> * Matrix<N,P> = Matrix<M,P>
  impl<const M: usize, const N: usize, const P: usize>
      Mul<Matrix<f64, N, P>> for Matrix<f64, M, N>
  {
      type Output = Matrix<f64, M, P>;

      fn mul(self, rhs: Matrix<f64, N, P>) -> Self::Output {
          // Standard matrix multiplication:
          // result[i][j] = sum over k of self[i][k] * rhs[k][j]
          todo!()
      }
  }
  ```

  > **Note:** The triple const generic signature `<const M: usize, const N: usize, const P: usize>` is the key insight -- the compiler verifies dimension compatibility at compile time. Your task: implement the multiplication loop.

## Notes
_Lesson not yet started._
