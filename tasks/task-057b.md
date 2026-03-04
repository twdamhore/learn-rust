# Lesson 057b: Smart Pointers Part B - PhantomData and Type-Level Markers

## Section 12: Smart Pointers & Interior Mutability

## Status: pending

## Added
- Split from original lesson 057 (overloaded ~2+ hrs)

## Objectives
- [ ] Use `PhantomData<T>` to indicate that a struct logically owns or relates to a type `T` even though it doesn't physically contain one, affecting drop checking and variance
- [ ] Understand why `PhantomData` is necessary: without it, the compiler sees no relationship between the struct and `T`, which can lead to incorrect variance inferences and unsound drop behavior
- [ ] Use `PhantomData` with the newtype pattern to create typed wrappers (like `Id<User>` vs `Id<Product>`) that are zero-cost at runtime but type-safe at compile time
- [ ] Understand covariance, contravariance, and invariance at a practical level: different `PhantomData` type parameters (e.g., `PhantomData<T>` vs `PhantomData<fn(T)>`) can affect what the compiler allows in terms of variance -- raw pointer variance details are deferred to lesson 073 (unsafe Rust)
- [ ] Compare with Java's generics (erased at runtime) and Go's lack of generics-before-1.18 -- Rust's PhantomData lets you carry type information with zero runtime cost

## Exercises
- [ ] **PhantomData for typed IDs**: Create a generic `Id<T>` struct (containing just a `u64`) that uses `PhantomData<T>` to tie it to a specific entity type. Define `User` and `Product` types. Show that `Id<User>` and `Id<Product>` are different types at compile time -- you cannot accidentally pass an `Id<User>` where an `Id<Product>` is expected. Verify with a function that only accepts `Id<User>` and observe the compile error when passing `Id<Product>`.
- [ ] **Type-safe units**: Create unit marker structs `Meters`, `Kilometers`, and `Seconds`. Build a `Quantity<U>` struct that holds an `f64` value and uses `PhantomData<U>` for the unit type. Implement `Add` only for same-unit quantities (adding `Quantity<Meters>` + `Quantity<Meters>` works, but `Quantity<Meters>` + `Quantity<Seconds>` is a compile error). Add a `convert` method from `Quantity<Meters>` to `Quantity<Kilometers>`.
- [ ] **PhantomData and lifetimes**: Create a struct `BorrowTracker<'a, T>` that holds owned data (`Vec<T>`) but uses `PhantomData<&'a T>` to tie the struct to a lifetime. This teaches how `PhantomData` communicates lifetime relationships to the compiler without raw pointers. Use the following pattern:
    ```rust
    use std::marker::PhantomData;

    // PhantomData tells the compiler this type "uses" lifetime 'a
    // even though no field directly holds a reference with that lifetime
    struct BorrowTracker<'a, T> {
        data: Vec<T>,
        _marker: PhantomData<&'a T>,
    }
    ```
    Implement a `new()` constructor and a `get()` method. Show that the compiler enforces the lifetime constraint: the `BorrowTracker` cannot outlive the lifetime `'a` it's tied to. Experiment with removing `PhantomData` and observe how the compiler's behavior changes.
- [ ] **Typestate builder with PhantomData [STRETCH]**: Create a `ConnectionBuilder` that uses zero-sized marker types (`NoHost`, `HasHost`, `NoPort`, `HasPort`) and `PhantomData` to enforce at compile time that `host()` and `port()` must be called before `connect()`. The `connect()` method should only exist on `ConnectionBuilder<HasHost, HasPort>`. Demonstrate that calling `connect()` without setting both values is a compile error.

## Notes
- Pin<T> content from the original lesson 057 has been moved to lesson 067 (advanced async) where it belongs, since Pin is hard to motivate without async context.
_Lesson not yet started._
