---
{"dg-publish":true,"permalink":"/atlas/typestate/","noteIcon":"","updated":"2024-10-29T17:52:28.624-07:00"}
---


## Example Implementations

### [[Atlas/MOCs/Rust\|Rust]]

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

### [[Typescript\|Typescript]]

```typescript
interface State1 { }
interface State2 { }


```

- https://catchts.com/type-state
- https://www.azavea.com/blog/2019/12/12/modeling-state-with-typescript/