# Rust hooks for pre-commit

[Rust](https://www.rust-lang.org) tools package for [pre-commit](https://pre-commit.com).

## Using rust tools with pre-commit

```yaml
- repo: https://github.com/Okm165/pre-commit-rust.git
    rev: master
    hooks:
      - id: cargo-check
      - id: cargo-clippy
        args:
          - "--fix"
          - "--allow-dirty"
      - id: cargo-fmt
```

## Using rust tools with pre-commit (specify path to Cargo.toml)

```yaml
-   - repo: https://github.com/Okm165/pre-commit-rust.git
    rev: master
    hooks:
      - id: cargo-check
        args:
          - "--manifest-path"
          - "<path to Cargo.toml>"
      - id: cargo-clippy
        args:
          - "--fix"
          - "--allow-dirty"
          - "--manifest-path"
          - "<path to Cargo.toml>"
      - id: cargo-fmt
        args:
          - "--manifest-path"
          - "<path to Cargo.toml>"
```
