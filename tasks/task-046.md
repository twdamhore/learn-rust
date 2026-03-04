# Lesson 046: Common std traits - Display, Debug, Default, From/Into

## Section 9: Generics & Traits

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Implement `std::fmt::Display` for custom types to control how they are printed with `{}`, and understand how it differs from `Debug` (which is for developers, `Display` is for users)
- [ ] Use the `Default` trait to provide sensible default values for structs, both via `#[derive(Default)]` and manual `impl Default`, and use it with struct update syntax and `Option::unwrap_or_default()`
- [ ] Implement `From<T>` for type conversions and understand that implementing `From` automatically gives you `Into` for free (blanket impl). Know the convention: implement `From`, call via `Into`
- [ ] Implement `TryFrom<T>` and `TryInto<T>` for fallible conversions that return `Result`, and choose between `From` (infallible) and `TryFrom` (fallible) based on whether the conversion can fail
- [ ] Recognize and use the ecosystem of common std traits: `Clone`, `PartialEq`/`Eq`, `PartialOrd`/`Ord`, `Hash` -- understanding when to derive vs manually implement

## Exercises
- [ ] **Display implementation**: Create a `Color` struct with `r`, `g`, `b` fields (u8). Implement `Display` to format as `#RRGGBB` hex string, and `Debug` (via derive) for developer output. Verify `println!("{}", color)` uses Display and `println!("{:?}", color)` uses Debug
- [ ] **Default with builder pattern**: Create a `Config` struct with 5+ fields, derive `Default`, and write a builder-style API. Show how `Config { name: "app".into(), ..Default::default() }` fills in remaining fields. Compare with Go's zero-value initialization
- [ ] **From/Into conversions**: Create `Celsius` and `Fahrenheit` tuple structs. Implement `From<Celsius> for Fahrenheit` and vice versa. Write code using `.into()` to convert between them. Then implement `From<Celsius> for f64` so temperatures can be used in arithmetic
- [ ] **TryFrom with validation**: Create an `Email` struct that can only be constructed from a valid email string. Implement `TryFrom<&str> for Email` that validates the string contains `@` and a domain. Return a custom error type on failure. Write tests for valid and invalid inputs. *Optional*: also implement `TryFrom<String> for Email` to see how the two impls differ
- [ ] **Derive vs manual impl [STRETCH]**: Create a `Point { x: f64, y: f64 }` struct. Derive `Clone` and `Debug`. Manually implement `PartialEq` to compare points within an epsilon tolerance (since `f64` equality is tricky). Explain why you cannot derive `Eq` or `Hash` for `f64` fields, and show how using `OrderedFloat` from the `ordered-float` crate would let you derive all of them

## Notes
> **Cross-reference**: Lesson 023 introduced `#[derive(Debug, Clone, PartialEq, Eq, Hash)]`. This lesson goes deeper: manual implementations, `Display`, `Default`, `From`/`Into`, `TryFrom`, and when derive is insufficient.

_Lesson not yet started._
