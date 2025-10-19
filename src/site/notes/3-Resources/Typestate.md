---
{"dg-publish":true,"permalink":"/3-resources/typestate/","tags":["☢️_Atomic","🌲_Evergreen","🔧_Technical"],"updated":"2025-10-19T09:22:15.078-07:00"}
---


## Example Implementations

### Rust

```rust
struct State { /* data here */}
struct TopLevelObject<S: TypeState> {
   state: Box<State>
   marker: PhantomData<S>
}

enum State1 {}
enum State2 {}

trait TypeState {}
impl TypeState for State1 { }
impl TyepState for State2 { }

impl TopLevelObject<State1> {
  fn new() -> Self { todo!() }
  fn next() -> TopLevelObject<State2> { todo!() }
}
```

- http://cliffle.com/blog/rust-typestate/
- [https://hoverbear.org/blog/rust-state-machine-pattern/#structures-with-transitions](https://hoverbear.org/blog/rust-state-machine-pattern/#structures-with-transitions)

### Typescript

```typescript
interface State1 { }
interface State2 { }


```

- https://catchts.com/type-state
- https://www.azavea.com/blog/2019/12/12/modeling-state-with-typescript/

## Related Concepts
- [[3-Resources/+MOCs/Rust\|Rust]] - Main MOC for Rust programming patterns
- [[3-Resources/Rust Development/Rust Compile Time Optimizations\|Rust Compile Time Optimizations]] - Performance optimization techniques
- [[3-Resources/Rust Development/Rust-Swift Interaction\|Rust-Swift Interaction]] - Cross-platform development patterns
