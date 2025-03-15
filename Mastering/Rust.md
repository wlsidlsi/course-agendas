**I. Introduction to Rust**

*   Understanding Rust's Core Principles
    *   Memory Safety without Garbage Collection
    *   Concurrency without Data Races
    *   Zero-cost Abstractions
*   Setting up a Rust Development Environment
    *   Installing Rust with `rustup`
    *   Understanding the Cargo Build System: `cargo new`, `cargo build`, `cargo run`, `cargo test`
    *   Choosing and Configuring a Code Editor (VS Code, IntelliJ IDEA, etc.)

**II. Basic Syntax and Data Types**

*   Variables and Mutability
    *   Declaring Variables with `let` and `const`
    *   Understanding Mutability with `mut`
    *   Shadowing Variables
*   Primitive Data Types
    *   Integers: `i8`, `i16`, `i32`, `i64`, `i128`, `u8`, `u16`, `u32`, `u64`, `u128`, `isize`, `usize`
    *   Floating-Point Numbers: `f32`, `f64`
    *   Booleans: `bool` (`true` or `false`)
    *   Characters: `char` (Unicode Scalar Values)
*   Compound Data Types
    *   Tuples: Creating, accessing elements
    *   Arrays: Fixed-size, elements of the same type
    *   Slices: Dynamically sized views into arrays
*   Operators
    *   Arithmetic Operators: `+`, `-`, `*`, `/`, `%`
    *   Comparison Operators: `==`, `!=`, `>`, `<`, `>=`, `<=`
    *   Logical Operators: `&&`, `||`, `!`
    *   Bitwise Operators: `&`, `|`, `^`, `!`, `<<`, `>>`
*   Control Flow
    *   `if` statements, `else if` blocks, `else` blocks
    *   `loop` keyword for indefinite loops
    *   `while` loops
    *   `for` loops: Iterating over ranges and collections
    *   `break` and `continue` keywords

**III. Ownership, Borrowing, and Lifetimes**

*   Understanding Ownership
    *   Each value in Rust has a variable that's called its owner
    *   There can only be one owner at a time
    *   When the owner goes out of scope, the value will be dropped
*   Borrowing
    *   Creating References with `&`
    *   Mutable References with `&mut`
    *   Rules of Borrowing: One mutable reference or multiple immutable references
    *   Dangling References
*   Lifetimes
    *   Purpose of Lifetimes: Ensuring references are always valid
    *   Lifetime Annotations: `'a`, `'static`
    *   Lifetime Elision Rules
    *   Lifetime Subtyping
*   Practical Examples
    *   Avoiding common ownership and borrowing errors
    *   Using lifetimes in function signatures and structs

**IV. Structs, Enums, and Pattern Matching**

*   Defining Structs
    *   Classic Structs: Named fields
    *   Tuple Structs: Named tuples
    *   Unit Structs: Fieldless structs
*   Methods
    *   Implementing Methods with `impl`
    *   The `self` Parameter
    *   Associated Functions
*   Enums
    *   Defining Enums with Variants
    *   Enums with Data: Holding data in variants
    *   Methods on Enums
*   Pattern Matching with `match`
    *   Matching on enum variants
    *   Matching on ranges
    *   Matching on tuples and structs
    *   The `_` wildcard
*   `if let` syntax

**V. Collections**

*   Vectors (`Vec<T>`)
    *   Creating Vectors: `Vec::new()`, `vec![]`
    *   Adding and Removing Elements: `push()`, `pop()`, `insert()`, `remove()`
    *   Iterating over Vectors
    *   Vector Capacity and Reallocation
*   Strings (`String`, `&str`)
    *   Creating Strings: `String::new()`, `String::from()`, `String::to_string()`
    *   Appending to Strings: `push_str()`, `push()`
    *   String Slicing
    *   Iterating over Strings: Characters, Bytes, Grapheme Clusters
*   Hash Maps (`HashMap<K, V>`)
    *   Creating Hash Maps: `HashMap::new()`
    *   Inserting and Retrieving Values: `insert()`, `get()`, `get_mut()`
    *   Iterating over Hash Maps
    *   Hash Functions and Custom Key Types

**VI. Error Handling**

*   Recoverable Errors with `Result<T, E>`
    *   The `Result` Enum: `Ok(T)` and `Err(E)`
    *   Handling `Result` with `match`
    *   Shortcuts: `unwrap()`, `expect()`, `is_ok()`, `is_err()`
    *   Propagating Errors with `?`
*   Unrecoverable Errors with `panic!`
    *   When to Panic
    *   Stack Unwinding vs. Aborting
    *   Setting `panic` behavior in `Cargo.toml`
*   Custom Error Types
    *   Defining Custom Error Enums or Structs
    *   Implementing the `Error` Trait

**VII. Generics, Traits, and Lifetimes**

*   Generics
    *   Generic Functions and Structs
    *   Type Parameters and Type Inference
    *   Generic Constraints with Traits
*   Traits
    *   Defining Traits
    *   Implementing Traits for Types
    *   Trait Objects: `dyn Trait`
    *   Default Implementations
    *   Deriving Traits with `#[derive(...)]`
*   Advanced Traits
    *   Associated Types
    *   Operator Overloading
    *   PhantomData

**VIII. Closures and Iterators**

*   Closures
    *   Defining Closures
    *   Closure Capture Modes: By reference, by mutable reference, by value
    *   `Fn`, `FnMut`, and `FnOnce` Traits
    *   Closures as Arguments and Return Values
*   Iterators
    *   The `Iterator` Trait
    *   Creating Iterators: `iter()`, `iter_mut()`, `into_iter()`
    *   Consuming Adapters: `map()`, `filter()`, `collect()`, `fold()`, `sum()`
    *   Iterator Chains
    *   Custom Iterators

**IX. Concurrency**

*   Threads
    *   Creating Threads with `thread::spawn()`
    *   Moving Ownership to Threads
    *   Waiting for Threads to Finish: `JoinHandle::join()`
*   Message Passing
    *   Channels: `mpsc` (Multiple Producer, Single Consumer)
    *   Creating Channels: `tx` (transmitter), `rx` (receiver)
    *   Sending and Receiving Messages
*   Shared-State Concurrency
    *   Mutexes (`Mutex<T>`)
    *   Atomically Reference Counted Pointers (`Arc<T>`)
    *   Read/Write Locks (`RwLock<T>`)
*   `Send` and `Sync` Traits

**X. Smart Pointers**

*   Box `<T>`
    *   Heap Allocation
    *   Ownership and Drop
*   Rc `<T>` and Arc `<T>`
    *   Reference Counting
    *   Shared Ownership
*   RefCell `<T>` and Mutex `<T>`
    *   Interior Mutability
    *   Runtime Borrowing Rules

**XI. Testing**

*   Writing Unit Tests
    *   The `#[test]` Attribute
    *   The `assert!` and `assert_eq!` Macros
    *   Organizing Tests in Modules
*   Integration Tests
    *   Creating an `tests` Directory
    *   Writing Integration Tests
*   Documentation Tests
    *   Writing Examples in Documentation Comments
    *   Running Documentation Tests

**XII. Macros**

*   Declarative Macros (Macros by Example)
    *   Defining Macros with `macro_rules!`
    *   Matching Patterns and Replacing with Code
    *   Hygiene
*   Procedural Macros
    *   Function-like Macros
    *   Derive Macros
    *   Attribute Macros
    *   Using `syn` and `quote` crates

**XIII. Asynchronous Programming with Async/Await**

*   Understanding Asynchronous Programming
    *   Futures
    *   Tasks
    *   Executors
*   Async/Await Syntax
    *   `async` Functions
    *   `await` Keyword
*   Using a Runtime
    *   `tokio`
    *   `async-std`
*   Writing Asynchronous Applications

**XIV. Unsafe Rust**

*   Understanding Unsafe Code
    *   Circumventing Rust's Safety Guarantees
    *   When to Use Unsafe Code
*   Unsafe Keywords
    *   `unsafe` Block
    *   `unsafe` Function
*   Common Unsafe Operations
    *   Dereferencing Raw Pointers
    *   Calling Unsafe Functions or Methods
    *   Creating Static Mutable Variables
    *   Implementing Unsafe Traits
    *   Accessing Fields of a `union`

**XV. FFI (Foreign Function Interface)**

*   Calling C Code from Rust
    *   Declaring External Functions with `extern`
    *   Data Type Conversions
    *   Memory Management
*   Calling Rust Code from C
    *   Making Rust Functions Callable from C
    *   Exporting C-compatible Interfaces
    *   Managing Memory Across the FFI Boundary
