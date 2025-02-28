# AIChat Development Guide

## Build and Test Commands
- Build: `cargo build` (debug) or `cargo build --release` (optimized)
- Run: `cargo run -- [args]` 
- Test all: `cargo test --all`
- Test single: `cargo test <test_name>`
- Test with output: `cargo test -- --nocapture`
- Lint: `cargo clippy --all --all-targets`
- Format: `cargo fmt --all` (check only: `cargo fmt --all --check`)

## Code Style Guidelines
- **Imports**: Group by local (with `crate::`) then external crates
- **Naming**: snake_case for variables/functions, CamelCase for types, SCREAMING_SNAKE_CASE for constants
- **Error Handling**: Use `anyhow`, `?` operator, and `.with_context()` for rich errors
- **Types**: Explicit type annotations, leverage `Option`/`Result` for safety
- **Structure**: Hierarchical modules with clear separation of concerns
- **Functions**: Descriptive verb names, boolean functions use `is_`/`has_` prefix
- **Documentation**: Add docs for public APIs and complex functions
- **State Management**: Use `Arc` and `RwLock` for shared state

Always maintain clean error handling with context for user-friendly messages.