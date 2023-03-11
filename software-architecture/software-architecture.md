# :heavy_check_mark: Software Architecture

## :round_pushpin: Introduction
`Software Architecture` refers to the fundametal organization of a software system and the key principles and decisions that guide its design and development. It encompasses the high-level structure of a software system and defines the components, relationships, and interactions between them.

It can be thought of as the blueprint for a software system, laying out the overall structure and design of the system before any code is written. It involves identifying the key components of the system, defining their responsibilities and interactions, and specifying the interfaces and protocols that govern how they communicate.

It is critical for building large, complex software systems that are *reliable*, *maintainable*, and *scalable*. It helps ensure the system is designed to meet the needs of its users and stakeholders, and that it can evolve and adapt over time as requirements change.

Software architecture is a board and multifaceted field, encompassing many approaches and methodologies. Some common architectural styles include `layered architecture`, `client-server architecture`, `microservices architecture`, and `event-driven architecture`. There are more.

## :round_pushpin: Design and Architecture
What are the differences between design and architecture? They are pretty much the same thing:
- `Architecture` is used in context of something at a high level that is separate from the lower-level details.
- `Design` implies structures and decisions at a lower level.

The low-level details and high-level decisions are all part of the same whole. They define the shape of the system.

[![Eisenhower matrix quote](https://quotes-github-readme.vercel.app/api?type=horizontal&theme=light&quote=The%20goal%20of%20software%20architecture%20is%20to%20minimize%20the%20human%20resources%20required%20to%20build%20and%20maintain%20the%20required%20system.&author=Robert%20C.%20Martin)](https://github.com/piyushsuthar/github-readme-quotes)

Developing fast is not necessarily the best way to build something. Overconfidence in developers can build over time, and the cost to maintain and develop more features will outweigh the benefit of more engineers/code.

This is why we need a design and architecture that minimize effort and maximize productivity.

## :round_pushpin: Two Values
Every software system provides two different values to the stakeholders: `behavior` and `structure`. Often one of the values is focused on over the other.

### Behavior
This value is to make systems behave in the way they're supposed to.

### Architecture
Behavior of machines must be easy to change. This is what `software` is supposed to help do.

The difficulty in making a change should be proportional only to the scope of the change and not to the *shape* of the change.

Architectures should be as **shape agnostic** as possible.

### Behavior vs Architecture
Which of these two values is more important? Is it more important for the software system to work? Or more important for the software system to be easy to change?

The former is the *wrong attitude*.

Some systems are impossible to change because the cost of change exceeds the benefits of the change.

### Eisenhower's Matrix
Matrix of importance versus urgency

[![Eisenhower matrix quote](https://quotes-github-readme.vercel.app/api?type=horizontal&theme=light&quote=I%20have%20two%20kinds%20of%20problems%2C%20the%20urgent%20and%20the%20important.%20The%20urgent%20are%20not%20important%2C%20and%20the%20important%20are%20never%20urgent.&author=Dwight%20D.%20Eisenhower)](https://github.com/piyushsuthar/github-readme-quotes)

![Picture of eisenhower matrix](images/eisenhower-matrix.png)

- Behavior is **urgent** but not always important.
- Architecture is **important** but never urgent.

Therefore there are 4 priorities:
1. Urgent and important.
2. Not urgent and important.
3. Urgent and not important.
4. Not urgent and not important.

Architecture pertains to 1 and 2. Behavior pertains to 1 and 3. Often business managers and devs elevate items in 3 to 1.

It is the responsibility of the development team to assert the importance of architecture over the urgency of features.

## :round_pushpin: Programming Paradigms
Paradigms are ways of programming, relatively unrelated to languages. A paradigm tells you which programming structures to use, and when to use them.

To date, there have been 3 paradigms. The paradigms are `structured programming`, `object-oriented programming`, and `functional programming`.

See more detailed explanation:
1. [Structured Programming](programming-paradigms/structured-programming.md)
2. [Object-Oriented Programming](programming-paradigms/object-oriented-programming.md)
3. [Functional Programming](programming-paradigms/functional-programming.md)

Each of these paradigms *removes* capabilities from the programmer. None of them adds new capabilities. Each imposes some kind of extra discipline that is *negative* in its intent. They tell us more what **not** to do than what we **can** do.

The three paradigms remove `goto` statements, function pointers, and assignment.

We use polymorphism to cross architectural boundaries. We use functional programming to impose discipline on the location of and access to data. We use structured programming as the algorithm foundation of our modules.

These three align with the three big concerns of architecture: `function`, `separation of components`, and `data management`.

## :round_pushpin: Design Principles
Good software systems begin with clean code. This is where the `SOLID` principles come in.

These principles tell us how to arrange functions and data structures into classes, and how those classes are connected. A class means a grouping of functions and data. The principles apply to these groupings.

The goal of these principles is to create mid-level software structures that:
- Tolerate change.
- Are easy to understand.
- Are the basis of components that can be used in many software systems.

The term "mid-level" means that these principles are applied by programmers working at the module level.

Here are the `SOLID` principles:
1. **[SRP: The Single Responsibility Principle](solid-principles/srp.md)**
    - Each software module has one, and only one, reason to change.
2. **[OCP: The Open-Closed Principle](solid-principles/ocp.md)**
    - For software systems to be easy to change, they must be designed to allow the behavior of those systems to be changed by adding *new* code, rathen than changing *existing* code.
3. **LSP: The Liskov Substitution Principle**
    - To build software systems from interchangeable parts, those parts must adhere to a contract that allows those parts to be substituted one for another.
4. **ISP: The Interface Segregation Principle**
    - Do not depend on things you *do not* use.
5. **DIP: The Dependency Inversion Principle**
    - Code that implements high-level policy should not depend on the code that implements low-level details. Rather, details should depend on policies.

## :round_pushpin: Key Points
Here are some key points to understand in architecture:
- Getting software to work is *easy*, but getting software **right** is **hard**.
- Writing messy code fast is always slower than staying clean.

## :round_pushpin: Supplemental Sources
1. [Clean Architecture: A Craftsman's Guide to Software Structure and Design [1st Edition] - Robert C. Martin](https://www.amazon.com/Clean-Architecture-Craftsmans-Software-Structure/dp/0134494164)
