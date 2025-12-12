# mork-rust-sdk

An official, asynchronous Rust SDK client for the Mork API, designed for robustness and ease of use in modern Rust applications.

---

## ✨ Features

* **Asynchronous:** Built on `reqwest` and `tokio` for high-performance, non-blocking API calls.
* **Safety:** Strongly typed data structures using `serde` for safe and easy JSON handling.
* **Convenience:** Handles URL construction and parameter encoding internally (`urlencoding`).

## 📥 Installation

Add the following to your project's `Cargo.toml` file:

```toml
[dependencies]
mork-rust-sdk = "0.1" # Use the latest version when publishing
tokio = { version = "1", features = ["full"] } # Required for running the async client