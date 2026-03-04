# Lesson 094: Memory layout - repr, alignment, size optimization

## Section 20: Special Targets

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Understand Rust's default struct layout (no guaranteed field order, compiler may reorder for optimal packing) vs `#[repr(C)]` which preserves declaration order with C-compatible padding
- [ ] Use `std::mem::size_of::<T>()`, `std::mem::align_of::<T>()`, and `std::mem::offset_of!()` to inspect type sizes, alignment requirements, and field offsets
- [ ] Know when and why to use `#[repr(packed)]` (remove padding, may cause unaligned access), `#[repr(transparent)]` (newtype with same layout as inner), and `#[repr(align(N))]` (force minimum alignment)
- [ ] Optimize struct sizes by reordering fields to minimize padding -- understand that a `(u8, u64, u8)` wastes more space than `(u64, u8, u8)` due to alignment requirements
- [ ] Understand enum layout: discriminant size, niche optimization (e.g., `Option<NonZeroU64>` is the same size as `u64`), and `#[repr(u8)]`/`#[repr(C)]` for enums

## Exercises
- [ ] **Exercise 1 - Struct Field Ordering**: Create several structs with fields in different orders (e.g., `struct A { a: u8, b: u64, c: u8 }` vs `struct B { b: u64, a: u8, c: u8 }`) and use `std::mem::size_of` and `std::mem::align_of` to compare their sizes and alignments -- explain why Rust's default repr may give different results than you'd expect from C
- [ ] **Exercise 2 - repr(C) Network Packet**: Write a `#[repr(C)]` struct that matches a C-style network packet header (e.g., version: u8, msg_type: u8, length: u16, sequence: u32, payload_size: u64) and verify its size and field offsets match what a C compiler would produce -- compare the size with the same fields in default Rust repr. (We use `msg_type` instead of `type` because `type` is a reserved keyword in Rust.)
- [ ] **Exercise 3 - Enum Niche Optimization**: **Note**: `NonZeroU64` is from `std::num` — it represents a `u64` that is guaranteed to never be zero. Rust uses this guarantee for niche optimization: `Option<NonZeroU64>` is the same size as `u64` because the `None` variant can use the zero value. Explore enum layout optimization: create `Option<Box<T>>`, `Option<NonZeroU64>`, `Option<&T>`, and `Option<bool>`, and print their sizes to observe niche filling -- then create a `#[repr(u8)]` enum and verify the discriminant is exactly 1 byte
- [ ] **Exercise 4 - Cache-Line Aware Struct**: Design a "cache-line aware" struct for a hypothetical hot loop: start with a poorly-ordered struct of mixed field sizes (10+ fields), measure its size, then reorder fields from largest alignment to smallest to minimize padding -- also try `#[repr(packed)]` and discuss when the tradeoff of potential unaligned access is worth it. **Warning**: `repr(packed)` can cause undefined behavior on architectures that require aligned memory access. Creating references to unaligned fields is UB in Rust. Use `addr_of!` or `read_unaligned` to safely access packed fields.

> **Note**: The `offset_of!` macro requires Rust 1.77+. Check your version with `rustc --version`.

## Notes
_Lesson not yet started._
