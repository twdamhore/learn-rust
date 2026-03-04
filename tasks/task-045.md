# Lesson 045: Trait objects - dyn Trait, vtables, object safety

## Section 9: Generics & Traits

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Understand dynamic dispatch: when you use `dyn Trait`, the compiler generates a vtable (virtual method table) and method calls are resolved at runtime via pointer indirection, unlike static dispatch which resolves at compile time
- [ ] Create trait objects using `Box<dyn Trait>` and `&dyn Trait`, and understand why trait objects must be behind a pointer (the compiler does not know their size at compile time). (Arc<dyn Trait> for thread-safe trait objects is covered in lesson 059.)
- [ ] Know the object safety rules: a trait is object-safe only if its methods do not use `Self` by value, do not use generic type parameters, and do not return `Self` (with some exceptions). Understand why these rules exist
- [ ] Compare static dispatch (generics/`impl Trait`: monomorphized, inlined, larger binary, faster) vs dynamic dispatch (`dyn Trait`: single function, smaller binary, vtable indirection overhead, flexible)
- [ ] Use trait objects to build heterogeneous collections and plugin-like architectures where you need to store or process values of different concrete types through a shared interface

**Quick note on `Box<T>`**: `Box::new(value)` allocates the value on the heap and gives you an owned pointer to it. We use `Box<dyn Trait>` for trait objects because the compiler doesn't know the concrete type's size at compile time. Full `Box<T>` coverage comes in lesson 058.

## Exercises
- [ ] **Heterogeneous collection**: Define a `Widget` trait with `fn render(&self) -> String` and `fn name(&self) -> &str`. Implement it for `Button`, `TextBox`, and `Checkbox`. Create a `Vec<Box<dyn Widget>>` containing all three and iterate to print each widget's name and rendered output
- [ ] **Object safety violation**: Add a method `fn duplicate(&self) -> Self` to your `Widget` trait and try to create a `Box<dyn Widget>` -- read and understand the object safety error. Fix it by returning `Box<dyn Widget>` instead of `Self`
- [ ] **Plugin system**: Build a simple plugin system: define a `Plugin` trait with `fn name(&self) -> &str` and `fn execute(&self, input: &str) -> String`. Create 3 plugins (e.g., UppercasePlugin, ReversePlugin, CensorPlugin), store them in a `Vec<Box<dyn Plugin>>`, and run each on user input
- [ ] **Static vs dynamic dispatch comparison [STRETCH]**: Write both a generic (static dispatch) version `fn process<T: Widget>(s: &T)` and a trait object (dynamic dispatch) version `fn process_dyn(s: &dyn Widget)` of the same function. Compile with `cargo build --release && ls -la target/release/your_binary` and compare binary sizes between the two approaches. Note which produces a larger binary and hypothesize why (hint: monomorphization vs vtable indirection)

## Notes
_Lesson not yet started._
