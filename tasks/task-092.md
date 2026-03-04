# Lesson 092: Property-Based Testing with proptest

## Section 18: Testing & Quality

## Status: pending

## Added
- Split from lesson 092 (v6 pacing review)

## Objectives
- [ ] Understand property-based testing vs example-based testing: instead of testing specific examples, describe properties that must hold for ALL inputs and let the framework generate thousands of test cases
- [ ] Set up the `proptest` crate and write property tests using built-in strategies (`any::<T>()`, ranges, regex strings, `prop_oneof!`)
- [ ] Use `proptest` strategies to generate complex test data: `prop::collection::vec()` for vectors, string regex strategies, and `prop_compose!` for custom composite strategies
- [ ] Understand shrinking and how to read proptest failure output: when a test fails, proptest automatically reduces the failing input to the minimal reproducing case

## Exercises
- [ ] **Exercise 1 -- Proptest a sort function**: Write a `my_sort(vec: Vec<i32>) -> Vec<i32>` function. Use proptest to verify: (1) output is sorted, (2) output has same length as input, (3) output contains exactly the same elements, (4) sorting twice gives the same result as sorting once. Generate vectors of varying lengths with `prop::collection::vec(any::<i32>(), 0..1000)`.
- [ ] **Exercise 2 -- Custom strategy with prop_compose!**: Define a `struct Order { id: u64, items: Vec<Item>, total: f64 }` and write a custom proptest strategy using `prop_compose!` that generates valid orders (total matches sum of item prices, at least 1 item, valid prices). Test a `validate_order` function against these generated orders.

  **Note**: When comparing `f64` totals in property tests, use approximate comparison (e.g., `(total - expected).abs() < 1e-10`) rather than exact equality, since floating-point arithmetic is not exact.
- [ ] **Exercise 3 -- Finding edge cases**: Create an `encode(input: &str) -> String` / `decode(encoded: &str) -> Result<String, DecodeError>` pair (e.g., run-length encoding). First write 3-4 example-based tests that pass. Then use proptest with `"[a-zA-Z0-9 ]{0,100}"` strategies to verify `decode(encode(s)) == Ok(s)` -- observe proptest finding edge cases your example tests missed. Examine the shrunk minimal failing case.

## Notes
_Lesson not yet started._
_Split from original lesson 092 which covered both proptest and cargo-fuzz (~1.75-2.5 hr estimated). This part focuses on proptest only._
