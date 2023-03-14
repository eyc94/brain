# :heavy_check_mark: The Test Boundary

## :round_pushpin: Introduction
The tests are part of the system and they participate in the architecture just like every part of the system does.

## :round_pushpin: Tests As System Components
There is confusion about tests. Are they part of the system? Are they separate? What kinds of tests?

From an architectural point of view, all tests are the same. They are architecturally equivalent.

Tests follow the Dependency Rule. They are detailed and concrete. They rely on the code being tested on. Nothing relies on the tests. You can think of the tests being the outermost circle of the architecture.

Tests are independently deployable. They are deployed in test systems, not production systems. In systems where independent deployment is not necessary, the tests will *still* be independently deployed.

Their role is to support development and *not* operations.

## :round_pushpin: Design For Testability
Most think that because of the reasons above, tests fall outside of the design of the system. This is wrong. If tests are not well-integrated into your system, your system will become fragile. It makes them rigid and hard to change.

The issue is coupling. Tests that are strongly coupled to the system must change with the system. Even the most trivial change to a system component can cause many coupled tests to break or need change.

Changes to common system components may cause hundred, or even thousands, or tests to break. This is the `Fragile Tests Problem`.

Imagine a tests suite that tests the GUI and interfaces on it. Imagine those interfaces change. This can cause many tests to break.

This makes the system rigid. Imagine making a change that breaks 1000+ tests. It makes the team hesitant to change it.

The solution is to design for testability. The first rule of design is to *not depend on things that are volatile*. A GUI is volatile. So don't write tests for it. Just write tests for the business rules.

## :round_pushpin: The Testing API
To accomplish this, create a specific API that the tests can use to verify all business rules. These tests should be able to avoid security constraints, bypass expensive resources, and force the system into particular testable states.

This API will be a superset of the suit of *interactors* and *interface adapters* that are used by the UI.

The testing API allows us to decouple tests from the app. This decoupling is more than just detaching the tests from the UI. The goal is to decouple the *structure* of the tests from the *structure* of the app.

### Structural Coupling
Structural coupling is one of the strongest, and most insidious, forms of test coupling. Imagine a suite that has a test class for every production class, and a set of test methods for every production method. This test suite is deeply coupled to the structure of the app.

When one production code changes, a *lot* of tests change with it. This makes the system rigid and tests fragile.

The role of the testing API is to *hide* the structure of the app from tests. This allows production code to be refactored to not affect tests. It also allows tests to be refactored to not affect production code.

Separation of evolution is needed. As time passes, the tests tend to become more concrete and specific. The production code tends to be more abstract and general. Structural coupling *impedes* this development. It prevents production code from being as general and flexible as it could be.

### Security
The testing API could be dangerous if deployed in production systems. The testing API could be kept separate in a different independently deployable component.
