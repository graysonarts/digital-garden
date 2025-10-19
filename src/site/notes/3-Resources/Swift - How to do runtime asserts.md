---
{"dg-publish":true,"permalink":"/3-resources/swift-how-to-do-runtime-asserts/","tags":["quicktip","swift","☢️_Atomic","🔧_Technical","🌲_Evergreen"],"updated":"2025-10-19T09:51:30.964-07:00"}
---


## How to do runtime asserts

```swift
        guard container != nil else {
            fatalError("This view needs a persistent container.")
        }
```