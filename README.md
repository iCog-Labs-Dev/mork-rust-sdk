# mork-rust-sdk

An official, asynchronous Rust SDK client for the Mork API, designed for robustness and ease of use in modern Rust applications.

This SDK allows Rust developers to programmatically perform core KG operations: transformation, import, upload, and complex querying.

---

## Key Features

| Feature | Description | Relevant Code |
| :--- | :--- | :--- |
| **Asynchronous Core** | Built on `tokio` and `reqwest`, ensuring non-blocking, high-performance network communication. | `MorkApiClient::dispatch` |
| **Request Trait** | Uses the `Request` trait to enforce a clear interface for all API calls (`path()`, `method()`, `body()`), enabling simple extension. | `pub trait Request` |
| **Metta Namespacing** | Provides first-class support for Metta/Hyperon-style hierarchical namespacing, crucial for managing KG context. | `struct Namespace` |
| **Data Operations** | Dedicated request builders for core Mork endpoints (`TransformRequest`, `UploadRequest`, `ExportRequest`, etc.). | `impl Request for ...` |

## Installation

Add the following to your project's `Cargo.toml` file:

```toml
[dependencies]
mork-rust-sdk = "0.1.0" # Current version
reqwest = { version = "0.11", features = ["json"] }
serde = { version = "1.0", features = ["derive"] }
tokio = { version = "1", features = ["rt-multi-thread", "macros"] }