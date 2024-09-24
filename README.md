# Mini Redis Client

This project is a Redis client built using the **Tokio** async runtime in Rust. The project follows the official [tokio.rs](https://tokio.rs) documentation, demonstrating the use of asynchronous programming, message-passing, and channels to build a Redis client with minimal dependencies.

## Features

- **Asynchronous Redis Client**: Uses Tokio's async runtime to handle Redis commands.
- **Concurrency**: Spawns multiple async tasks that communicate via channels.
- **Message Passing**: Utilizes Tokio's `mpsc` channels for inter-task communication, avoiding direct sharing of the Redis client across tasks.
- **Minimal**: Follows a simple architecture while still demonstrating key async patterns in Rust.

## Requirements

- **Rust** (version >= 1.56)
- **Tokio**: Tokio provides the async runtime used in this project. Add it to your `Cargo.toml`.
  
```toml
[dependencies]
tokio = { version = "1", features = ["full"] }
mini-redis = "0.4"
bytes = "1"
