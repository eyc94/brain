# :heavy_check_mark: LSP: The Liskov Substitution Principle

## :round_pushpin: Introduction
Barbara Liskov wrote the following about subtypes:

>*What is wanted here is something like the following substitution property: If for each object o1 of type S there is an object o2 of Type T such that for all programs P defined in terms of T, the behavior of P is unchanged when o1 is substituted for o2 then S is a subtype of T.*

## :round_pushpin: Guiding The Use Of Inheritance
![Image of a sample license class](../images/solid-principles/lsp/license-class.png)

We have a class called `License`. It has a method called `calcFee()`, which is called by the `Billing` application. There are two "subtypes" of `License`. These are `PersonalLicense` and `BusinessLicense`.

Both subtypes are substitutable for the `License` type, so it *does not matter* which type the `Billing` application will use.

## :round_pushpin: The Square/Rectangle Problem
![Image of the square rectangle example](../images/solid-principles/lsp/square-rectangle-example.png)

`Square` is *not* a proper subtype of `Rectangle` because the height and width of the `Rectangle` are *independently mutable*. The height and width of a `Square` must *change together*. The `User` might believe it is communicating with a `Rectangle` and get confused.

```java
Rectange r = ...
r.setW(5);
r.setH(2);
assert(r.area() == 10);
```

If the `...` code actually produced a `Square`, the assertion would fail. This is because *not all* rectangles can be squares.

A way to defend against this, we can add checks to the `User` that checks whether the `Rectangle` is actually a `Square`. The behavior of the `User` now depends on the *types* it uses, so those types are **not** substitutable.

