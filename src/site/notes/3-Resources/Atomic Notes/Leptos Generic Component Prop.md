---
{"dg-publish":true,"permalink":"/3-resources/atomic-notes/leptos-generic-component-prop/","tags":["☢️","rust","software","programming"],"updated":"2025-10-18T21:23:28.266-07:00"}
---

```rust
progress: impl Fn() -> i32 + 'static
```

To accept both signals and derived signals, you specify the prop as a generic `impl` trait