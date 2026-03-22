# mork-rust-sdk

An official, asynchronous Rust SDK for the **Mork API**, designed for robustness and ease of use in modern Rust applications.

This SDK allows Rust developers to programmatically perform core KG operations: transformation, import, upload, export, and complex querying.

---

## Key Features

| Feature | Description | Relevant Code |
| :--- | :--- | :--- |
| **Asynchronous Core** | Built on `tokio` and `reqwest` for non-blocking, high-performance network communication. | `MorkApiClient::dispatch` |
| **Request Trait** | Provides a `Request` trait defining `path()`, `method()`, and `body()`, making it easy to add new endpoints. | `pub trait Request` |
| **Metta Namespacing** | Supports Metta/Hyperon-style hierarchical namespacing for precise KG context management. | `struct Namespace` |
| **Data Operations** | Provides request builders for core Mork endpoints: `TransformRequest`, `UploadRequest`, `ExportRequest`, `ImportRequest`, and more. | `impl Request for ...` |
| **Doctests & Unit Tests** | Fully tested SDK ensures correctness for both pattern/template operations and HTTP requests. | `#[cfg(test)] mod tests` |

---

## Installation

Add the following to your project's `Cargo.toml`:

```toml
[dependencies]
mork-rust-sdk = "0.2.1" # Latest version
reqwest = { version = "0.11", features = ["json"] }
serde = { version = "1.0", features = ["derive"] }
tokio = { version = "1", features = ["rt-multi-thread", "macros"] }