---
{"dg-publish":true,"permalink":"/efforts/the-rust-garden/adding-stripe-subscriptions-to-rust-axum/","tags":["rust","axum","stripe","payment"],"updated":"2024-11-30T09:23:25.457-08:00"}
---

1. Introduction of what subscriptions are
2. How features/entitlements allow you to simplify the code base
3. `async-stripe` doesn't currently support entitlements
4. A basic implementation to catch webhooks and fetch entitlements
5. Caching Entitlements
6. Using entitlements in your code