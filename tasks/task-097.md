# Lesson 097: Serde - Serialize/Deserialize, JSON, TOML, custom

## Section 19: Ecosystem & Tooling

## Status: pending

## Added
- Initial curriculum design

## Objectives
- [ ] Derive `Serialize` and `Deserialize` on structs and enums using serde, and understand what the derive macro generates under the hood
- [ ] Use `serde_json` to serialize Rust types to JSON and deserialize JSON strings/files back into Rust types, handling errors with `serde_json::Error`
- [ ] Use the `toml` crate to read and write TOML configuration files, a common pattern in Rust CLI tools and services
- [ ] Customize serialization behavior with serde attributes: `#[serde(rename)]`, `#[serde(default)]`, `#[serde(skip)]`, `#[serde(flatten)]`, `#[serde(tag)]`, `#[serde(untagged)]`
- [ ] Write a custom `Deserialize` implementation for a type that needs special parsing logic (e.g., deserializing a date string into a custom `Date` struct)

**Note on `DeserializeOwned`**: In generic functions, you'll see `T: DeserializeOwned` instead of `T: Deserialize<'de>`. `DeserializeOwned` means the type can be deserialized without borrowing from the input data (it owns all its data). Use it in generic contexts where the input lifetime is not available.

## Exercises
- [ ] **Exercise 1 -- JSON roundtrip**: Define a `#[derive(Serialize, Deserialize)]` struct `ApiResponse<T: Serialize + DeserializeOwned>` with fields `status: u16`, `message: String`, `data: Option<T>`, and a nested `User` struct with `name`, `email`, `age`. Serialize to JSON, deserialize back, and verify equality. Test with `data: None` and `data: Some(user)`.
- [ ] **Exercise 2 -- TOML config**: Create an `AppConfig` struct with nested sections (`database: DbConfig`, `server: ServerConfig`, `logging: LogConfig`). Write a sample `config.toml` file. Deserialize it into `AppConfig` using `toml::from_str`. Add `#[serde(default)]` for optional fields so missing keys get sensible defaults. Serialize the config back to TOML and compare.
- [ ] **Exercise 3 -- Serde attributes**: Create an enum `Event` with variants `UserCreated { user_id: u64, name: String }`, `OrderPlaced { order_id: u64, total: f64 }`, `SystemAlert(String)`. Use `#[serde(tag = "type", content = "payload")]` for adjacently tagged representation. Add `#[serde(rename_all = "camelCase")]`. Serialize each variant and verify the JSON shape. Then try `#[serde(untagged)]` and compare.
- [ ] **Exercise 4 [STRETCH] -- Custom deserializer**: Create a `struct HexColor { r: u8, g: u8, b: u8 }` that should deserialize from a JSON string like `"#FF8800"`. Implement `Deserialize` manually (using a visitor or `deserialize_with`) to parse the hex string. Also implement `Serialize` to produce the `"#RRGGBB"` format. Write tests that round-trip through JSON.

## Notes
_Lesson not yet started._
