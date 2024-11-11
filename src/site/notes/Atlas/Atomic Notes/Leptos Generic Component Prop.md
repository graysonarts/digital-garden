---
{"dg-publish":true,"permalink":"/atlas/atomic-notes/leptos-generic-component-prop/","tags":["☢️","rust","software","programming"],"updated":"2024-11-09T09:23:23.052-08:00"}
---

```rust
progress: impl Fn() -> i32 + 'static
```

To accept both signals and derived signals, you specify the prop as a generic `impl` trait