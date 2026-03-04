# Lesson 036: Vec<T> - creating, updating, accessing, memory model

## Section 8: Collections & Iterators

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Create vectors using `vec![]` macro, `Vec::new()`, and `Vec::with_capacity()`, understanding when to pre-allocate
- [ ] Modify vectors with `push`, `pop`, `insert`, `remove`, `extend`, `retain`, and `truncate`
- [ ] Access elements safely with `.get()` (returns `Option`) vs indexing with `[]` (can panic), and understand the trade-offs
- [ ] Understand Vec's memory model: pointer + length + capacity on the stack, data on the heap, and how reallocation works when capacity is exceeded
- [ ] Iterate over vectors with `for`, `.iter()`, `.iter_mut()`, and `.into_iter()`, understanding ownership implications of each
- [ ] Compare `Vec<T>` with Java's `ArrayList<T>` and Go's slices (backing array, length, capacity)

## Exercises
- [ ] **Exercise 1 - Capacity observation**: Create an empty `Vec<i32>`, then push 20 elements one at a time. After each push, print `len()` and `capacity()`. Observe the growth pattern (doubling). Then create a `Vec::with_capacity(20)` and do the same, noting that no reallocation occurs
- [ ] **Exercise 2 - Safe vs unsafe access**: Create a `Vec<String>` with 5 elements. Access index 2 with `[]` and with `.get(2)`. Then access index 10 with both methods. Handle the `None` from `.get()` gracefully. Explain in a comment why `.get()` is preferred in production code
- [ ] **Exercise 3 - Stack with Vec**: Implement a simple stack (`push`, `pop`, `peek`, `is_empty`, `size`) using `Vec<T>` as the backing store. Then (optional extension if time permits) use it to check if parentheses are balanced in a string like `"((()))"` vs `"(()""`
- [ ] **Exercise 4 - Sorting and deduplication**: Build a function `fn unique_sorted(input: Vec<i32>) -> Vec<i32>` that returns a sorted vector with duplicates removed. Use `.sort()`, `.dedup()`. Also implement it using `.sort_unstable()` and compare. Test with `vec![3, 1, 4, 1, 5, 9, 2, 6, 5, 3]`

## Notes
_Lesson not yet started._
