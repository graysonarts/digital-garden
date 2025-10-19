---
{"dg-publish":true,"permalink":"/3-resources/atomic-notes/leptos-generic-component-prop/","tags":["☢️_Atomic","rust","software","programming","🔧_Technology"],"updated":"2025-10-18T23:01:29.098-07:00"}
---

```rust
progress: impl Fn() -> i32 + 'static
```

To accept both signals and derived signals, you specify the prop as a generic `impl` trait