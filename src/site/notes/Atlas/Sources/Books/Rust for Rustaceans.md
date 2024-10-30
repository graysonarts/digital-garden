---
{"dg-publish":true,"permalink":"/atlas/sources/books/rust-for-rustaceans/","tags":["sources/books","rust"],"noteIcon":"","updated":"2024-10-29T17:59:14.394-07:00"}
---


# Rust for Rustaceans

![rw-book-cover](https://m.media-amazon.com/images/I/8194Ew8gVrS._SY160.jpg)

## Metadata
- Author: [[Jon Gjengset\|Jon Gjengset]]
- Full Title: Rust for Rustaceans
- Category: #resource/books

## Highlights
- Nearly every type can, and should, implement Debug, even if it only prints the type’s name. ([Location 1572](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=1572))
- Tied in close second are the Rust auto-traits Send and Sync (and, to a lesser extent, Unpin). If a type does not implement one of these traits, it should be for a very good reason. ([Location 1575](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=1575))
- If your types cannot implement them, make sure that fact, and the reason why, is well documented! ([Location 1580](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=1580))
- The next set of nearly universal traits you should implement is Clone and Default. ([Location 1581](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=1581))
- One step further down in the hierarchy of expected traits is the comparison traits: PartialEq, PartialOrd, Hash, Eq, and Ord. ([Location 1585](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=1585))
- PartialOrd and Hash are more specialized, and may not apply quite as broadly, but where possible you will want to implement them too. ([Location 1589](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=1589))
- Finally, for most types, it makes sense to implement the serde crate’s Serialize and Deserialize traits. ([Location 1595](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=1595))
- Most libraries therefore choose to provide a serde feature that adds support for serde only when the user opts into it. ([Location 1598](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=1598))
- when you define a new trait, you’ll usually want to provide blanket implementations as appropriate for that trait for &T where T: Trait, &mut T where T: Trait, and Box<T> where T: Trait. You may be able to implement only some of these depending on what receivers the methods of Trait have. ([Location 1612](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=1612))
- For any type that can be iterated over, consider implementing IntoIterator for both &MyType and &mut MyType where applicable. ([Location 1616](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=1616))
- These traits allow you to have a value of type T and call methods on some type U by calling them directly on the T-typed value if T: Deref<Target = U>. ([Location 1621](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=1621))
- If you provide a relatively transparent wrapper type (like Arc), there’s a good chance you’ll want to implement Deref so that users can call methods on the inner type by just using the . operator. ([Location 1623](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=1623))
- In general, Borrow is intended only for when your type is essentially equivalent to another type, whereas Deref and AsRef are intended to be implemented more widely for anything your type can “act as.” ([Location 1636](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=1636))
- In Rust, restrictions usually come in the form of trait bounds and argument types, and promises come in the form of trait implementations and return types. ([Location 1654](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=1654))
- In most cases it pays off to use generics rather than concrete types, to allow the caller to pass any type that conforms to what your function actually needs, rather than only a particular type. ([Location 1680](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=1680))
- A good rule of thumb is to make an argument generic if you can think of other types a user might reasonably and frequently want to use instead of the concrete type you started with. ([Location 1687](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=1687))
- It may be tempting to start your interfaces off with concrete types and then turn them generic over time. This can work, but keep in mind that such changes are not necessarily backward compatible. ([Location 1702](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=1702))
- You should prefer your traits to be object-safe even if that comes at a slight cost to the ergonomics of using them (such as taking impl AsRef<str> over &str), since object safety enables new ways to use your traits. ([Location 1713](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=1713))
- If the code you write needs ownership of the data, such as to call methods that take self or to move the data to another thread, it must store the owned data. ([Location 1738](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=1738))
- On the other hand, if your code doesn’t need to own the data, it should operate on references instead. ([Location 1742](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=1742))
- Other times, reference lifetimes complicate the interface so much that it becomes a pain to use. If your users are struggling to get code to compile on top of your interface, that’s a sign that you may want to (even unnecessarily) take ownership of certain pieces of data. ([Location 1749](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=1749))
- For that reason, we need to provide best-effort cleanup through Drop. If cleanup errors, at least we tried—we swallow the error and move on. If an executor is still available, we might spawn a future to do cleanup, but if it never gets to run, we did what we could. ([Location 1761](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=1761))
- It’s therefore critical for you to make it as easy as possible for users to understand your interface and as hard as possible for them to use it incorrectly. The two primary techniques at your disposal for this are your documentation and the type system, so let’s look at each of those in turn. ([Location 1799](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=1799))
- First, clearly document any cases where your code may do something unexpected, or where it relies on the user doing something beyond what’s dictated by the type signature. ([Location 1808](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=1808))
- Second, include end-to-end usage examples for your code on a crate and module level. ([Location 1812](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=1812))
- Third, organize your documentation. Having all your types, traits, and functions in a single top-level module makes it difficult for the user to get a sense of where to start. ([Location 1822](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=1822))
- The first of these is semantic typing, in which you add types to represent the meaning of a value, not just its primitive type. ([Location 1835](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=1835))
- A closely related technique is to use zero-sized types to indicate that a particular fact is true about an instance of a type. ([Location 1843](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=1843))
- if your function ignores a pointer argument unless a given Boolean argument is true, it’s better to combine the two arguments instead. With an enum type with one variant for false (and no pointer) and one variant for true that holds a pointer, neither the caller nor the implementer can misunderstand the relationship between the two. ([Location 1867](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=1867))
- Another small but useful tool in making interfaces obvious is the #[must_use] annotation. Add it to any type, trait, or function, and the compiler will issue a warning if the user’s code receives an element of that type or trait, or calls that function, and does not explicitly handle it. ([Location 1871](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=1871))
- Whether you’re adding a new type, field, method, or trait implementation or changing an existing one, you want to make sure that the change will not break existing users’ code, and that you are planning to keep that change around for a while. ([Location 1878](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=1878))
- The fewer public types you have, the more freedom you have to change things later without breaking existing code. ([Location 1886](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=1886))
- Rust provides the #[non_exhaustive] attribute to help mitigate these issues. You can add it to any type ([Location 1904](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=1904))
- definition, and the compiler will disallow the use of implicit constructors (like lib::Unit { field1: true }) and nonexhaustive pattern matches (that is, patterns without a trailing , ..) on that type. ([Location 1905](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=1905))
- Removing a trait implementation is a breaking change, but implementing traits for a new type is never a problem, since no crate can have implementations that conflict with that type. ([Location 1915](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=1915))
- Most changes to existing traits are also breaking changes, such as changing a method signature or adding a new method. ([Location 1928](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=1928))
- A sealed trait is one that can be used only, and not implemented, by other crates. ([Location 1932](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=1932))
- You should seal a trait only if it does not make sense for a foreign crate to implement your trait; ([Location 1937](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=1937))
- The trick is to add a private, empty trait as a supertrait of the trait you wish to seal ([Location 1948](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=1948))
- Sometimes, changes you make to one part of your code affect the contract elsewhere in your interface in subtle ways. The two primary ways this happens are through re-exports and auto-traits. ([Location 1956](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=1956))
- To mitigate issues like this, it’s often best to wrap foreign types using the newtype pattern, and then expose only the parts of the foreign type that you think are useful. ([Location 1972](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=1972))
- In many cases, you can avoid the newtype wrapper altogether by using impl Trait to provide only the very minimal contract to the caller. ([Location 1973](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=1973))
- if you have a public type A that contains a private type B, and you change B so that it is no longer Send, then A is now also not Send. That is a breaking change! ([Location 1998](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=1998))
- To catch these cases before they happen, it’s good practice to ([Location 2001](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=2001))
- include some simple tests in your test suite that check that all your types implement these traits the way you expect. ([Location 2001](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=2001))
- fn is_normal<T: Sized + Send + Sync + Unpin>() {} #[test] fn normal_types() {   is_normal::<MyType>(); } ([Location 2004](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=2004))
- Testing that a type implements a set of traits ([Location 2006](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=2006))
- You have two main options for representing errors: enumeration and erasure. ([Location 2037](https://readwise.io/to_kindle?action=open&asin=B0957SWKBS&location=2037))
