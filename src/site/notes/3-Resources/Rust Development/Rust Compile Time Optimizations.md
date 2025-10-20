---
{"dg-publish":true,"permalink":"/3-resources/rust-development/rust-compile-time-optimizations/","tags":["🌱_Active","rust","quicktip","🔧_Technical","🗒️_Note"],"updated":"2025-10-19T09:29:07.470-07:00"}
---


-  **LLD linker**: The [[Rust\|Rust]] compiler spends a lot of time in the "link" step. LLD is _much faster_ at linking than the default [[Rust\|Rust]] linker. To install LLD, find your OS below and run the given command [^1]:

    -   **Ubuntu**: `sudo apt-get install lld`

    -   **Arch**: `sudo pacman -S lld`

    -   **Windows**: Ensure you have the latest [cargo-binutils](https://github.com/rust-embedded/cargo-binutils)

        ```sh
        cargo install -f cargo-binutils
        rustup component add llvm-tools-preview
        ```

    -   **MacOS**: You can follow this [instructions](https://lld.llvm.org/MachO/index.html) to install lld manually or install llvm through brew which includes lld: `brew install llvm`

[^1]: https://bevyengine.org/learn/book/getting-started/setup/

## Related Concepts
- [[Rust\|Rust]] - Main MOC for Rust programming resources
- [[3-Resources/Rust Development/Typestate\|Typestate]] - Advanced Rust patterns for state management
- [[3-Resources/Rust Development/Rust-Swift Interaction\|Rust-Swift Interaction]] - Cross-platform development considerations
