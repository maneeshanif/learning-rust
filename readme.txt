
# Cargo: Rust's Build System and Package Manager
## Create a New Rust Project with Cargo
 To create a new project with Cargo, use the command:


## `` cargo new hello_cargo ``


## What Does Cargo Generate?
Running the above command creates a new folder with the following structure:

- **`src` folder**: This is where your Rust code lives (e.g., main.rs).
- **`.gitignore`** file: Automatically added for Git projects.
- **Optional files**: If you want to add files like `README.md` or a license, keep them outside the `src` folder since it’s meant exclusively for your working code.
- **`Cargo.toml`** file: Works like package.json in JavaScript. It tracks your project’s dependencies and version info.



## Building with Cargo
To compile your Rust project, use:


`cargo build` 

This command creates a `target` folder containing:

- `Cargo.lock`: A file that ensures consistent dependency versions.
- `debug` **folder**: Contains your compiled code, including the hello_cargo.exe file.

## What Rust's Official Docs Say:
**"This command creates an executable file in` target/debug/hello_cargo` (or `target\debug\hello_cargo.exe` on Windows) rather than in your current directory. Because the default build is a debug build, Cargo puts the binary in a directory named debug."**

## Running Your Code
After building, you can run your code using:


`.\target\debug\hello_cargo.exe`

However, this command is long and repetitive. Rust offers a simpler way:


`cargo run`

### Key Commands in Cargo
Here’s a quick overview of essential Cargo commands:

1. `cargo new hello_cargo`: Initialize a new Rust project.
2. `cargo build`: Compile your code (required initially).
3. `cargo run`: Combine build and execution into one command.
4. `cargo check`: Quickly validate your code without creating an executable (useful for CI/CD pipelines).
5. `cargo build --release`: Create an optimized production build.
***
## *Why Use `cargo run`?*
The `cargo run` command eliminates the two-step process of building and running your code. It automatically compiles any changes and executes your program in one step.
***

## `cargo check`: A Fast Way to Validate Code
The `cargo check` command ensures your code compiles but skips creating an executable. This is faster than `cargo build` and perfect for iterative coding.
***

## From Rust's Official Docs:
**"Often, `cargo check` is much faster than `cargo build` because it skips producing an executable. Many Rustaceans run `cargo check` periodically while writing code to quickly ensure it compiles."**
***

## Building for Production
By default, `cargo build` creates a **debug build**. For production-ready, optimized code, use:


## `` cargo build --release ``

This command creates a `release` folder inside `target``. Although optimized builds are faster at runtime, they take slightly longer to compile.

## Development vs. Release Profiles
Rust uses two profiles:

1. **Development**: Faster compilation but less optimized.
2. **Release**: Highly optimized for performance and suitable for final production builds.


## Authors

- [@maneeshanif](https://www.github.com/maneeshanif)