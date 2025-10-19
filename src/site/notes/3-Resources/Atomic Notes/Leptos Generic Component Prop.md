---
{"dg-publish":true,"permalink":"/3-resources/atomic-notes/leptos-generic-component-prop/","tags":["☢️_Atomic","rust","software","programming","🔧_Technical","🌲_Evergreen"],"updated":"2025-10-19T09:17:59.344-07:00"}
---

```rust
progress: impl Fn() -> i32 + 'static
```

To accept both signals and derived signals, you specify the prop as a generic `impl` trait