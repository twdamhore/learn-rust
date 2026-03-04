_**SUPERSEDED**: This lesson has been split into [Lesson 83a](task-083a.md) and [Lesson 83b](task-083b.md). Use those files instead._

# Lesson 083: Property-based testing (proptest), fuzzing (cargo-fuzz)

## Section 18: Testing & Quality

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Understand property-based testing philosophy: instead of testing specific examples, describe properties that must hold for ALL inputs and let the framework generate thousands of test cases
- [ ] Use the `proptest` crate to generate random test inputs with strategies (`any::<T>()`, ranges, regex, `prop_oneof!`, custom strategies)
- [ ] Write meaningful property checks that capture invariants (e.g., "sorting is idempotent", "encode then decode returns original", "output length <= input length")
- [ ] Set up `cargo-fuzz` for fuzz testing to discover crashes, panics, and edge cases in parsing/deserialization code
- [ ] Interpret proptest shrinking output to find minimal failing cases and use the persistence file to reproduce failures

## Exercises
- [ ] **Exercise 1 -- Proptest a sort function**: Write a `my_sort(vec: Vec<i32>) -> Vec<i32>` function. Use proptest to verify: (1) output is sorted, (2) output has same length as input, (3) output contains exactly the same elements, (4) sorting twice gives the same result as sorting once. Generate vectors of varying lengths (0..=1000) with `prop::collection::vec(any::<i32>(), 0..1000)`.
- [ ] **Exercise 2 -- Roundtrip property**: Create an `encode(input: &str) -> String` / `decode(encoded: &str) -> Result<String, DecodeError>` pair (e.g., run-length encoding). Use proptest with `any::<String>()` and `"[a-zA-Z0-9 ]{0,100}"` strategies to verify that `decode(encode(s)) == Ok(s)` for all inputs. Intentionally introduce a bug and observe proptest's shrinking find the minimal failing case.
- [ ] **Exercise 3 -- Custom strategy and complex data**: Define a `struct Order { id: u64, items: Vec<Item>, total: f64 }` and write a custom proptest strategy that generates valid orders (total matches sum of item prices, at least 1 item, valid prices). Use `prop_compose!` to build the strategy. Test a `validate_order` function against these generated orders.
- [ ] **Exercise 4 -- Fuzzing a parser**: Write a simple `fn parse_key_value(input: &[u8]) -> Result<(String, String), ParseError>` that parses `key=value` from raw bytes. Set up `cargo-fuzz` with a fuzz target that feeds random bytes to this parser. Run the fuzzer briefly and document any panics or unexpected behaviors found. Fix the issues and re-run.

## Notes
_Lesson not yet started._
