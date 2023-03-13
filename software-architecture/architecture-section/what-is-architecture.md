# :heavy_check_mark: What is Architecture?

## :round_pushpin: Introduction
The word "architecture" is powerful. It makes us think of decisions and technical prowess. When we think of a software architect, we think of someone who has power and who commands respect. This is what we, as young devs, aspire to be one day.

But what is software architecture? What do software architects do, and when do they do it?

Software architects are just programmers. They are the best programmers. They may not code as much as a regular programmer, but they still code.

The architecture of a software system is the shape given to that system by those who build it. The form of that shape is in the division of that system into components, the arrangement of those components, and the ways those components interact with each other.

This is to help develop, deploy, operate, and maintain the system.

>*The strategy behind that facilitation is to leave as many options open as possible, for as long as possible*.

Architecture does not play a role in whether a system works or not. A bad architecture in a system can still work. The primary purpose of architecture is to support the life cycle of the system.

Good architectures make the system easy to understand, easy to develop, easy to maintain, and easy to deploy. The goal is to minimize lifetime cost of the system and maximize programmer productivity.

## :round_pushpin: Development
The architecture of a system should make that system easy to develop.

In small teams, no one cares about the architecture because it is seen as an impediment. Teams just want to get things to work and get them done. That is why most systems lack good architecture. They began with none.

In a larger team with a larger system, developers cannot make progress unless the system is divided into well-defined components with stable interfaces. It might be so that teams are divided into the number of components.

This is not really the best way, but teams will gravitate towards this architecture over time if they are driven by development schedule.

## :round_pushpin: Deployment
To be effective, a software system must be deployable. It should not cost much to deploy. A goal of architecture should be to make a system that can be easily deployed *with a single action*.

However, deployment is not really considered in the beginning. So, deployability takes precedence. This leads to architectures that make the system easy to develop but hard to deploy.

For example, a team might consider using a `micro-services architecture` in the beginning because it make clear boundaries between components, and it makes the system easy to develop. But, when it comes time to deploy, there are way too many micro-services to deploy and connect and time with one another.

If architects considered deployment early, they might have created fewer services, a hybrid of services and in-process components, and a better way to manage interconnections.

## :round_pushpin: Operation
Architecture impacts operation less than development, deployment, and maintenance. This is because operation problems can be solved by using more hardware.

Hardware is relatively cheap nowadays. So, architecture has much less of an impact on operation.

However, architecture plays another role in operation of a system. A good software architecture communicates the operational needs of the system.

The architecture of a system makes the operation of the system apparent to the devs. Architecture should reveal operation. It should elevate the use cases, the features, and the required behaviors of the system to first-class entities that are visible landmarks for devs.

This simplifies the understanding of the system. This helps in development and maintenance.

## :round_pushpin: Maintenance
Maintenance is the **most** costly.

This is the constant parade of new features, defects, and corrections that consumes most of the developer's time.

The cost of maintenance is in *spelunking* and risk. Spelunking is the cost of digging through the existing software to try and find the best place to put the new feature or fix the bug.

Doing this also creates inadvertent defects, which creates risk.

A carefully thought out architecture mitigates these risks. It creates clear boundaries and shows the path for future features, reducing risks.

## :round_pushpin: Keeping Options Open
There are two values of software: behavior and structure. Structure is the more important.

Software allows us to quickly change behavior of machines. But this flexibility depends on the shape of the system, arrangement of the components, and how they are interconnected.

We want to keep software soft by leaving as many options as open as possible. What do we need to leave open? *The details that do not matter*.

All systems can be decomposed into two major elements: `policy` and `details`.

Policy embodies all the business rules and procedures. The policy is where the tru value of the system lives.

Details enable humans, other systems, and programmers to communicate with the policy. They do not impact the policy at all. These are IO devices, databases, web systems, servers, frameworks, communication protocols, etc.

The goal of the architect is to create a shape for the system that knows policy is the most important while making details irrelevant to that policy. This allows decisions about those details to be *delayed* and *deferred*.

For example:
- It is *not* necessary to choose a database system in the beginning of development because high-level policy **should not** care which kind of database will be used. It should not care if it is relational, distributed, hierarchical, or flat files.
- It is *not* necessary to choose a web server early in development because the high-level policy should not know that it is being delivered over the web. *You don't even need to deliver over the web*.
- It is *not* necessary to adopt REST early because the high-level policy should be agnostic about the interface to the outside world. We do not need to adopt a micro-services framework, or SOA framework.
- It is *not* necessary to adopt a dependency injection framework early because the high-level policy should not care how dependencies are resolved.

***If you can develop the high-level policy without committing to the details that surround it, you can delay and defer decisions for a long time***.

The longer you wait, the more information you will have to *properly* make those decisions.

You can also experiment if you have a working high-level policy and it is agnostic.

The longer you leave options open, the more experiments you can run, the more things you can try, and thte more information you will have to make a decision later when you can no longer defer.

What if the decisions have already been made? What if your company/team made a commitment to a database, or web server, or framework? ***A good architect pretends that the decision has not been made***, and shapes the system such that those decisions can still be deferred or changed for as long as possible.

>*A good architect maximizes the number of decisions not made*.

## :round_pushpin: Device Independence
Long ago, code was written *directly* on IO devices. The code was *device dependent*. What happens if the device the code depends on changes?

For example, from code punching cards to code using magnetic tape.

Those programs had to be rewritten to accomodate the use of magnetic tapes as the IO device.

`Device Independence` was invented in the 1960s. Now, the same program can read/write cards or read/write tape, *without any change*. The `Open-Closed Principle (OCP)` was born (but not yet named).
