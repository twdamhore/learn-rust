# Lesson 071b: Procedural Macros - Part B: Function-Like and Advanced Derive

## Section 15: Macros

## Status: pending

## Added
- Split from lesson 071 (v6 pacing review)

## Objectives
- [ ] Write function-like proc macros that accept custom syntax
- [ ] Parse custom syntax with `syn` (custom parsing beyond `DeriveInput`)
- [ ] Handle errors in proc macros (compile_error!, span diagnostics)
- [ ] Build a more complex derive macro with guided architecture

## Exercises
- [ ] **Function-like make_struct!**: Write a function-like macro `make_struct!` that generates a struct definition from a DSL; e.g., `make_struct!(Point { x: f64, y: f64 })` generates the struct with `Debug` and `Clone` derives; use custom `syn::parse::Parse` implementation
  Hint: In `quote!`, you can generate derive attributes like: `quote! { #[derive(Debug, Clone)] struct #name { ... } }`

  > **`syn::parse::Parse` minimal example:**
  > ```rust
  > use syn::{parse::{Parse, ParseStream}, Ident, Token, Type, Result};
  >
  > struct FieldDef { name: Ident, ty: Type }
  >
  > impl Parse for FieldDef {
  >     fn parse(input: ParseStream) -> Result<Self> {
  >         let name: Ident = input.parse()?;        // parse an identifier
  >         input.parse::<Token![:]>()?;              // parse the `:` token
  >         let ty: Type = input.parse()?;            // parse a type
  >         Ok(FieldDef { name, ty })
  >     }
  > }
  > ```
- [ ] **[STRETCH] Derive Builder (guided)**: Implement a `#[derive(Builder)]` macro that generates a builder pattern -- a builder struct with setter methods for each field and a `build()` method returning the original struct; this is a follow-the-guide exercise with provided architecture (field iteration, Option wrapping, error handling for missing fields). _(This is a substantial exercise inspired by the dtolnay proc-macro-workshop. If you reach 90 minutes after completing make_struct!, defer this to a follow-up session.)_

  **Provided scaffold** -- Follow the architecture below. The derive macro should support usage like this:

  ```rust
  #[derive(Builder)]
  struct Command {
      executable: String,
      args: Vec<String>,
      current_dir: String,
  }

  // Generated API:
  let cmd = Command::builder()
      .executable("cargo".into())
      .args(vec!["build".into()])
      .current_dir(".".into())
      .build()
      .unwrap();
  ```

  **Step-by-step architecture:**

  1. **Parse the struct** -- Use `DeriveInput` to get the struct name and extract its named fields.
  2. **Generate a builder struct** -- Create `FooBuilder` with every field wrapped in `Option<T>` (all initialized to `None`).
  3. **Generate setter methods** -- For each field, generate a method that takes the field value, sets the `Option`, and returns `&mut Self`.
  4. **Generate `build()` method** -- Check that every field is `Some`; if any is `None`, return `Err(String)` saying which field is missing; otherwise construct the original struct.
  5. **Generate `builder()` associated function** -- Add an `impl OriginalStruct` block with a `fn builder() -> OriginalStructBuilder` that returns a new builder with all fields `None`.

  **Starter code skeleton:**

  ```rust
  use proc_macro::TokenStream;
  use quote::quote;
  use syn::{parse_macro_input, DeriveInput, Data, Fields};

  #[proc_macro_derive(Builder)]
  pub fn derive_builder(input: TokenStream) -> TokenStream {
      let input = parse_macro_input!(input as DeriveInput);
      let name = &input.ident;
      let builder_name = syn::Ident::new(&format!("{}Builder", name), name.span());

      // Step 1: Extract named fields
      let fields = match &input.data {
          Data::Struct(data) => match &data.fields {
              Fields::Named(fields) => &fields.named,
              _ => panic!("Builder only supports structs with named fields"),
          },
          _ => panic!("Builder only supports structs"),
      };

      // Step 2: Generate Option-wrapped fields for the builder
      // TODO: iterate over `fields` and create Option<FieldType> versions

      // Step 3: Generate setter methods
      // TODO: for each field, generate fn field_name(&mut self, val: FieldType) -> &mut Self

      // Step 4: Generate build() method
      // TODO: check each field is Some, construct the original struct

      // Step 5: Generate the builder() associated function on the original struct
      // TODO: impl Name { fn builder() -> NameBuilder { ... } }

      todo!("Fill in the steps above")
  }
  ```

## Notes
_Lesson not yet started._
