# :heavy_check_mark: Component Cohesion

## :round_pushpin: Introduction
Which classes belong in which component? This decision depends on the context. There are three principles of component cohesion:
1. **REP:** The Reuse/Release Equivalence Principle
2. **CCP:** The Common Closure Principle
3. **CRP:** The Common Reuse Principle

## :round_pushpin: The Reuse/Release Equivalence Principle
>*The granule of reuse is the granule of release*.

In this day, there are a lot of module management tools like `Maven`, `Leiningen`, and `RVM`. This is because a lot of reusable components and component libraries were created. We are living in an age of software reuse.

The REP means people who want to reuse software components cannot, and will not, do so unless those components are tracked through a release process and have release numbers.

This is because devs need to know when changes are coming and what changes those new releases will bring.

The dev should have the power to use the new release or the old release. So, the release process must make appropriate notifications and release documentation so that users can make decisions.

So, the classes and modules that are formed into a component must belong to a cohesive group. There must be a common theme that all those modules share. It can't just be random modules and classes.

They should also be *releasable* together.

It is easy to detect **violations** of REP.
