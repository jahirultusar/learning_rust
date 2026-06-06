# Guessing Game: [Chapter 2] (https://doc.rust-lang.org/book/ch02-00-guessing-game-tutorial.html)

A short, console-based game built in Rust where the player tries to guess a randomly generated number between 1 and 100. This project covers core Rust fundamentals from Chapter 2 of the official Rust book.

## Key Rust Concepts in this chapter

### 1. Library Imports (`use`)
* `std::io`: Handles user input and console output.
* `std::cmp::Ordering`: An enum with variants `Less`, `Greater`, and `Equal` used for comparing values.
* `rand::Rng`: A trait that defines methods for random number generators.

### 2. Variable Mutability and Shadowing
* `let secret_number`: Immutable by default. Stores the target number.
* `let mut guess`: Explicitly mutable (`mut`) to allow the string to change as the user types.
* **Shadowing**: The code re-declares `let guess: u32`. This converts the original string input into an unsigned 32-bit integer, reusing the variable name.

### 3. Error and Input Handling
* `io::stdin().read_line(&mut guess)`: Reads keyboard input and appends it to the string.
* `.expect()`: A crash safeguard that handles potential input failures.

### 4. Control Flow and Pattern Matching
* `loop`: Creates an infinite loop so the player can keep guessing until they win.
* `match guess.trim().parse()`: Uses pattern matching to handle the result of string-to-number conversion.
    * `Ok(num)`: Valid number found, returns the value.
    * `Err(_)`: Invalid input found, ignores the error and restarts the loop (`continue`).
* `match guess.cmp(&secret_number)`: Compares the guess to the secret number and prints the result.
* `break`: Ends the loop and exits the program when the player guesses correctly.
