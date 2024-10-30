---
{"dg-publish":true,"permalink":"/atlas/rust-compile-time-optimizations/","tags":["🌱","rust","quicktip"],"noteIcon":"","updated":"2024-10-29T17:38:12.541-07:00"}
---


-  **LLD linker**: The [[Atlas/MOCs/Rust\|Rust]] compiler spends a lot of time in the "link" step. LLD is _much faster_ at linking than the default [[Atlas/MOCs/Rust\|Rust]] linker. To install LLD, find your OS below and run the given command [^1]:
    
    -   **Ubuntu**: `sudo apt-get install lld`
        
    -   **Arch**: `sudo pacman -S lld`
        
    -   **Windows**: Ensure you have the latest [cargo-binutils](https://github.com/rust-embedded/cargo-binutils)
        
        ```sh
        cargo install -f cargo-binutils
        rustup component add llvm-tools-preview
        ```
        
    -   **MacOS**: You can follow this [instructions](https://lld.llvm.org/MachO/index.html) to install lld manually or install llvm through brew which includes lld: `brew install llvm`

[^1]: https://bevyengine.org/learn/book/getting-started/setup/