# Lesson 082: Unsafe functions, unsafe traits, unsafe impl

## Section 16: Unsafe & FFI

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Write `unsafe fn` functions and understand that callers must ensure preconditions (documented as `# Safety` sections)
- [ ] Implement `unsafe trait`s (like `Send` and `Sync`) and understand when `unsafe impl` is needed
- [ ] Wrap unsafe code inside safe public APIs -- the "unsafe sandwich" pattern where unsafe internals are hidden behind a safe interface
- [ ] Document safety invariants using `# Safety` doc comments on unsafe functions and `// SAFETY:` comments on unsafe blocks
- [ ] Study how `unsafe` is used internally in `std` types like `Vec`, `String`, and `slice`

## Exercises
- [ ] **Unsafe function with invariants**: Write an `unsafe fn get_unchecked(slice: &[i32], index: usize) -> i32` that indexes without bounds checking using `*slice.as_ptr().add(index)`; document the `# Safety` requirement that `index < slice.len()`; write tests that use it correctly and add a commented-out test showing UB
- [ ] **Unsafe trait implementation**: Define a trait `ZeroInitializable` (marked `unsafe trait`) for types that are safe to initialize with all-zero bytes; implement `unsafe impl ZeroInitializable for u32` and `unsafe impl ZeroInitializable for f64`; write a generic function `fn zero_init<T: ZeroInitializable>() -> T` that uses `std::mem::zeroed()`
  Think about why `String` or `bool` should NOT implement `ZeroInitializable` -- what invariants would all-zero bytes violate?
- [ ] **Safe wrapper**: Write a `SafeBuffer` struct using a fixed-capacity stack buffer (this uses const generics -- `<const N: usize>` lets the buffer size be a compile-time parameter, similar to arrays `[T; N]`):
  ```rust
  struct SafeBuffer<const N: usize> {
      data: [u8; N],
      len: usize,
  }
  ```
  Internally, use `get_unchecked` and `get_unchecked_mut` in unsafe blocks for the implementation. Provide safe public methods: `push(&mut self, byte: u8) -> Result<(), ()>` (bounds-checks before unsafe write), `get(&self, index: usize) -> Option<u8>` (bounds-checks before unsafe read), and `as_slice(&self) -> &[u8]` (returns `&data[..len]`). The point is the "unsafe sandwich" -- unsafe internals wrapped in a safe API that upholds all invariants. Test the safe API thoroughly, including full-buffer and out-of-bounds cases.

  > **Note**: Const generics (`<const N: usize>`) are used here as a preview — they're formally covered in lesson 089. The syntax is straightforward: the generic parameter is a compile-time constant value rather than a type.

- [ ] **Study std source**: Use the Rust docs to look at the source of `Vec::push` and `String::from_utf8_unchecked`; write comments in your code summarizing what unsafe operations they perform and what invariants they maintain

## Notes
_Lesson not yet started._
