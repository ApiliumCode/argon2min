<p align="center">
  <img src="https://raw.githubusercontent.com/ApiliumCode/aingle/main/assets/aingle.svg" alt="AIngle Logo" width="200"/>
</p>

<h1 align="center">argon2min</h1>

<p align="center">
  <strong>Minimal Argon2 password hashing for the AIngle ecosystem</strong>
</p>

<p align="center">
  <a href="https://crates.io/crates/argon2min"><img src="https://img.shields.io/crates/v/argon2min.svg" alt="Crates.io"/></a>
  <a href="https://docs.rs/argon2min"><img src="https://docs.rs/argon2min/badge.svg" alt="Documentation"/></a>
  <a href="https://github.com/ApiliumCode/argon2min/blob/main/LICENSE"><img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="License"/></a>
  <a href="https://github.com/ApiliumCode/argon2min/actions"><img src="https://github.com/ApiliumCode/argon2min/workflows/CI/badge.svg" alt="CI Status"/></a>
</p>

---

## Overview

A pure Rust implementation of the Argon2 password hashing algorithm, providing both Argon2i and Argon2d variants. This library is designed for secure password hashing and password-based key derivation within the AIngle distributed systems framework.

## Features

- **Pure Rust** - No C dependencies, safe and portable
- **Argon2i** - Side-channel resistant, recommended for password hashing
- **Argon2d** - Faster variant for non-interactive scenarios
- **Constant-time verification** - Prevents timing attacks
- **Zero-on-drop** - Sensitive data is securely erased from memory

## Installation

Add to your `Cargo.toml`:

```toml
[dependencies]
argon2min = "0.1"
```

## Usage

```rust
use argon2min;

fn main() {
    let password = "secure_password";
    let salt = "random_salt_value";

    // Argon2i - recommended for password hashing
    let hash = argon2min::argon2i_simple(password, salt);

    println!("Hash: {}", hex::encode(&hash));
}
```

## Variants

| Variant | Use Case | Security |
|---------|----------|----------|
| **Argon2i** | Password hashing, key derivation | Side-channel resistant |
| **Argon2d** | Cryptocurrency, non-interactive | Faster, data-dependent |

## Part of AIngle

This crate is part of the [AIngle](https://github.com/ApiliumCode/aingle) ecosystem - a Semantic DAG framework for IoT and distributed AI applications.

## References

- [Argon2 Specification (PDF)](https://github.com/P-H-C/phc-winner-argon2/raw/master/argon2-specs.pdf)
- [PHC Winner Argon2](https://github.com/p-h-c/phc-winner-argon2)

## License

Licensed under the MIT License. See [LICENSE](LICENSE) for details.

---

<p align="center">
  <sub>Maintained by <a href="https://apilium.com">Apilium Technologies</a> - Tallinn, Estonia</sub>
</p>
