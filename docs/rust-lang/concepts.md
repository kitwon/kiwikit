---
tags: rust-lang
---

# Generics

## Where clauses

#rust can use [traits as parameters](https://doc.rust-lang.org/book/ch10-02-traits.html#traits-as-parameters). And `where` clause is apply bounds to arbitrary types, rather than just to type parameters.

* When specifying generics types and bounds separately is clearer:

```rust
impl <A: TraitB + TraitC, D: TraitE + TraitF> MyTrait<A, D> for YourTypes {}

// Expression bounds with a `where` clause
impl <A, D> MyTrait for YourTypes where
  A: TraitB + TraitC,
  D: TraitE + TraitF
  {

  }
```