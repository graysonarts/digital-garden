---
{"dg-publish":true,"permalink":"/atlas/swift/","tags":["quicktip","swift"],"updated":"2024-10-29T17:53:20.144-07:00"}
---


## How to do runtime asserts

```swift
        guard container != nil else {
            fatalError("This view needs a persistent container.")
        }
```