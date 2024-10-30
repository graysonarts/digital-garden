---
{"dg-publish":true,"permalink":"/atlas/swift/","tags":["quicktip","swift"]}
---


## How to do runtime asserts

```swift
        guard container != nil else {
            fatalError("This view needs a persistent container.")
        }
```