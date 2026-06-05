# Learning Rust 🦀

My personal journey learning Rust using the official book, *The Rust Programming Language*. This repository contains all the follow-along projects and exercises managed under a single Cargo workspace.

## 📁 Repository Structure

The project uses a Cargo workspace to keep everything organized within a single repository:

- `projects/` — Contains all the individual chapter projects and applications.
- `Cargo.toml` — The root workspace configuration that manages all projects together.

## 🚀 How to Run the Projects

You can run any specific project directly from the root directory using the `-p` (package) flag:

```bash
# For example, run the Chapter 2 Guessing Game
cargo run -p guessing_game
```

To run tests for a specific project:
```bash
cargo test -p <project_name>
```

Happy Learning :) 