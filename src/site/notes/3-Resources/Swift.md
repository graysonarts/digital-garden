---
{"dg-publish":true,"permalink":"/3-resources/swift/","tags":["quicktip","swift"],"updated":"2025-10-18T21:23:27.981-07:00"}
---


## How to do runtime asserts

```swift
        guard container != nil else {
            fatalError("This view needs a persistent container.")
        }
```