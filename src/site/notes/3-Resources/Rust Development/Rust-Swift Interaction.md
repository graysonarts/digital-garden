---
{"dg-publish":true,"permalink":"/3-resources/rust-development/rust-swift-interaction/","tags":["rust","swift","🔧_Technology"],"updated":"2025-10-18T23:01:54.285-07:00"}
---


## How does storage work in swift?

Storage is done with [CoreData](https://developer.apple.com/documentation/coredata/)

> Core Data abstracts the details of mapping your objects to a store, making it easy to save data from Swift and Objective-C without administering a database directly.

`CoreData` must be added the the XCode Project to be usable.

The `CoreData` stack consists of:
> An instance of [`NSManagedObjectModel`](https://developer.apple.com/documentation/coredata/nsmanagedobjectmodel) represents your app’s model file describing your app’s types, properties, and relationships.
> An instance of [`NSManagedObjectContext`](https://developer.apple.com/documentation/coredata/nsmanagedobjectcontext) tracks changes to instances of your app’s types.
> An instance of [`NSPersistentStoreCoordinator`](https://developer.apple.com/documentation/coredata/nspersistentstorecoordinator) saves and fetches instances of your app’s types from stores.
> An instance of [`NSPersistentContainer`](https://developer.apple.com/documentation/coredata/nspersistentcontainer) sets up the model, context, and store coordinator all at once.

During startup, initialize the `NSPersistentContainer`

```swift
    lazy var persistentContainer: NSPersistentContainer = {
        let container = NSPersistentContainer(name: "DataModel")
        container.loadPersistentStores { description, error in
            if let error = error {
                fatalError("Unable to load persistent stores: \(error)")
            }
        }
        return container
    }()
```

Once initialized, it contains the rest of the `CoreData` Stack.

The root view's controller's container should point to the `NSPersistentContainer` that was created during app initialization (maybe?)

`NSPersistentContainer` is meant to be subclassed to create your data model.

The `CoreData` model consists of Entities, Attributes, and Relationships. XCode has an interface for defining all of these things and it generates code as a result.

An [Entity](https://developer.apple.com/documentation/coredata/modeling_data/configuring_entities) has [Attributes](https://developer.apple.com/documentation/coredata/modeling_data/configuring_attributes) and Entities relate to each other through [Relationships](https://developer.apple.com/documentation/coredata/modeling_data/configuring_relationships).

Relationships are basically like joins in SQL.

An Entity becomes a [NSManagedObject](https://developer.apple.com/documentation/coredata/nsmanagedobject)

If I want to support syncing across devices (probably not in v1), I will need to use [CloudKit](https://developer.apple.com/documentation/coredata/mirroring_a_core_data_store_with_cloudkit) which handles the syncing automatically. The `CoreData` backend needs to be an `NSSqliteStoreType` in order to support `CloudKit` so it makes sense to only use that store type for this.

`UniFFI-rs` provides a bindgen style interface for Swift and other languages. https://mozilla.github.io/uniffi-rs/

## Related Concepts
- [[3-Resources/+MOCs/Rust\|Rust]] - Main MOC for Rust programming resources
- [[3-Resources/Rust Development/The Rust Garden/Typestate\|Typestate]] - Advanced Rust patterns for state management
- [[3-Resources/Rust Development/Rust Compile Time Optimizations\|Rust Compile Time Optimizations]] - Performance optimization techniques
