---
{"dg-publish":true,"permalink":"/3-resources/rust-development/rust-on-esp-32/","tags":["rust","embedded","esp32"],"updated":"2025-10-18T21:23:28.107-07:00"}
---


## Definitions

**ESP-NOW** 

## std vs no_std

**std** is a richer environment, providing access to everything that IDF handles. Abstracts a bunch of stuff

**no_std** still supports WiFI/BLE/ESP-NOW which is good, more direct hardware access, smaller footprint and real-time

## Setting up for development

Most of the newer devices are RISC-V, so follow these instructions: https://docs.esp-rs.org/book/installation/riscv.html

For **std** applications, follow https://docs.esp-rs.org/book/installation/std-requirements.html also

Maybe consider using containers: https://docs.esp-rs.org/book/installation/using-containers.html

```shell
cargo install cargo-espflash espflash ldproxy
cargo install probe-rs --features cli
```

```shell
apt install clang libclang-dev
```
## Starting a new project
- [`esp-template`](https://github.com/esp-rs/esp-template) - `no_std` template.
- [`esp-idf-template`](https://github.com/esp-rs/esp-idf-template) - `std` template.

```shell
cargo generate esp-rs/esp-idf-template
```

## Resources / References
- https://docs.esp-rs.org/book
- https://github.com/esp-rs/awesome-esp-rust
- https://doc.rust-lang.org/nightly/rustc/platform-support/esp-idf.html - Support IDF