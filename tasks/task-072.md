# Lesson 072: Attribute macros, real-world macro patterns

## Section 15: Macros

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Write attribute macros that transform function or struct definitions (e.g., adding logging, timing, or validation)
- [ ] Study how real-world attribute macros work: `#[tokio::main]`, `#[serde(rename)]`, `#[test]`
- [ ] Combine derive macros and attribute macros (helper attributes) to create configurable derives
- [ ] Know when to choose macros vs generics/traits: macros for code generation, traits for polymorphism, generics for type-level abstraction

## Exercises
- [ ] **#[log_calls] attribute macro**: Write an attribute macro that wraps a function body to print the function name and arguments before execution and the return value after; apply it to several functions and verify the output
- [ ] **Study #[tokio::main]**: Use `cargo expand` on a `#[tokio::main] async fn main()` to see what the attribute macro generates; write a comment explaining the expansion (it creates a `fn main` that builds a runtime and blocks on the async body)
- [ ] **Validation attribute**: Write an attribute macro `#[validate_positive]` for functions that take numeric parameters; the macro inserts assertions at the start of the function body to check that all numeric args are positive; test with both valid and invalid inputs

  **Starter code** -- syn::ItemFn parsing scaffold:
  ```rust
  use proc_macro::TokenStream;
  use quote::quote;
  use syn::{parse_macro_input, ItemFn, FnArg, PatType, Pat};

  #[proc_macro_attribute]
  pub fn validate_positive(_attr: TokenStream, item: TokenStream) -> TokenStream {
      let input_fn = parse_macro_input!(item as ItemFn);

      // Extract function signature details
      let fn_name = &input_fn.sig.ident;
      let fn_args = &input_fn.sig.inputs;
      let fn_body = &input_fn.block;
      let fn_vis = &input_fn.vis;
      let fn_sig = &input_fn.sig;

      // Iterate over parameters to find numeric ones
      let checks = fn_args.iter().filter_map(|arg| {
          if let FnArg::Typed(PatType { pat, .. }) = arg {
              if let Pat::Ident(pat_ident) = pat.as_ref() {
                  let name = &pat_ident.ident;
                  // Generate a runtime check for this parameter
                  return Some(quote! {
                      if #name < 0 {
                          panic!("{} must be positive, got {}", stringify!(#name), #name);
                      }
                  });
              }
          }
          None
      });

      // Reconstruct the function with validation checks prepended
      let output = quote! {
          #fn_vis #fn_sig {
              #(#checks)*
              #fn_body
          }
      };

      output.into()
  }
  ```

  > **Note:** This scaffold shows the basic structure. Your task: refine it to only check numeric parameter types (i32, i64, f64, etc.) rather than all parameters.
- [ ] **Macro vs trait comparison**: Implement the same feature two ways -- a `Describe` trait that returns a string description of a struct; first with a derive macro that generates it automatically from field names/types, then with a manual trait impl; compare the trade-offs in a code comment

## Notes
_Lesson not yet started._
