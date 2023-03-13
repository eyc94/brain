# :heavy_check_mark: Independence

## :round_pushpin: Introduction
A good architecture must support:
- The use cases and operation of the system.
- The maintenance of the system.
- The development of the system.
- The deployment of the system.

## :round_pushpin: Use Cases
The architecture of the system **must** support the intent of the system.

If system is a shopping cart app, the architecture must support shopping cart use cases.

However, architecture does not wield much influence over the behavior of the system. Architecture should clarify and expose behavior so the intent of the system is visible at the architectural level.

A shopping cart app with a good architecture will *look* like a shopping cart app. Developers do not have to hunt for behaviors because the behaviors will be first-class elements at the top level. They will have functions and classes with clear names that describe what they do.

## :round_pushpin: Operation
Architecture plays a bigger role in operation of a system. The system must allow the general use case throughput/output. For example, allowing the system to scale/work with many users.

How to achieve this is a decision the architect leaves open.

An architecture that maintains isolation of components and that does not assumme means of communication between components will be better suited to adapt to the operational needs of the system change over time.

## :round_pushpin: Development
Architecture plays a role in supporting development.

>*Any organization that designs a system will produce a design whose structure is a copy of the organization's communication structure*.

A system that is developed by many teams and devs need to have their concerns in mind. It also must be designed so their concerns don't conflict with those of the other teams.

This is done by partitioning the system into isolated components. Then, those components can be given to teams.

## :round_pushpin: Deployment
The architecture also determines how easy it is to deploy. The goal is "immediate deployment".

The architecture should not rely on scripts and property file tweaks. It should be immediately deployable after build.

## :round_pushpin: Leaving Options Open
A good architecture balances all of these concerns. However, balancing is hard.

We don't know what all the use cases are. We don't know the operational constraints, team structure, or deployment requirements.

Even if we knew them, these change throughout the lifecycle.

## :round_pushpin: Decoupling Layers
Consider the use cases. The architect wants the system to support all cases, but we have no prior knowledge of that.

However, the architect *does* know the intent of the system. So, they can employ the SRP and the CCP to separate those things that change for different reasons. Also, to collect those things that change for the same reasons.

What changes for different reasons? Consider UIs. UIs change for reasons that have nothing to do with business rules. So, it's good to separate these so they can be changed independently of one another.

Business rules can also be separated amongst themselves. The rules closely tied to the app, and the rules in general. These two change at different rates and reasons, so they should be separated.

The database, query language, and the schema are details that have nothing to do with business rules or the UI. They should also be separated to be changed independently.

So, our system is divided into horizontal layers: the UI, the app-specific business rules, app-independent rules, and the database (there are more).

## :round_pushpin: Decoupling Use Cases
Use cases change for different reasons. They are a natural way to divide the system.

These use cases cut through our horizontal layers *verically*. So every use cases uses some UI, some business rules, and some database functionality.

We keep the use cases *separate* down the vertical height of the system. So if we have an *add order* use case and a *delete order* use case, these are decoupled in *each* layer.

## :round_pushpin: Decoupling Mode
The decoupling helps with operations. Operations that run on high throughput are probably already separated from those that run on low throughput. If the UI and database is already separate, they can run in different servers because there is already the separation.

Notice how the decoupling we did on the use cases helps with operations. To take advantage of benefit, decoupling must have the appropriate mode.

To run in separate servers, the components cannot share address space of a processor. They must be independent services. These are called `micro-services`. An architecture based on services is called `Service-Oriented Architecture (SOA)`.

## :round_pushpin: Independent Develop-ability
As long as the layers and use cases are decoupled, the architecture will support the organization of the teams, regardless of whether they are organized as feature teams, component teams, layer teams, etc.

## :round_pushpin: Independent Deployability
It should also give flexibility in deployment. It should be possible to hot-swap layers and use cases in running systems.

## :round_pushpin: Duplication
We should reduce duplication whenever we can.

There are two types of duplicates: *true* and *false/accidental*.

The true duplicates are where every change requires the same change to every duplicate of that instance. A false duplication is two duplicated sections of code that evolve along different paths (i.e. change at different rates and for different reasons).

Resist the temptation to eliminate *every* duplication just because it *looks* and *feels* the same. Make sure it is real!

## :round_pushpin: Decoupling Modes (Again)
There are many ways to decouple layers and use cases. They can be decoupled at code level, at binary code (deployment) level, and at execution unit (service) level.
- **Source level:** We can control dependencies between code modules so that changes to one does not cause recompilation of another. Components all execute in the same address space, and they communicate with function calls. There is a single executable. This is a `monolithic structure`.
- **Deployment level:** We can control dependencies between deployable units so that changes to the code in one do not force other to be rebuilt and redeployed. They may be in the same address space and communicate through different mediums. It just matters that they are independently deployable units.
- **Service level:** We can reduce dependences down to the level of data structures and communicate through network packets such that every execution unit is entirely independent of source and binary changes to others.

What is the best mode?

It is tough to determine at an early stage of a project. But as the project matures, it is easier to see what it needs.

A popular approach is service level decoupling. However, this is pretty expensive to do.

A good architecture will allow the system to be born as a monolith, deployed in a single file, but then grow into a set of independently deployable units, and then all the way to independent services and/or micro-services. As thing change, it should also allow for reversing that progression and sliding back to a monolith.

It is good to leave the decoupling mode as an open option.
