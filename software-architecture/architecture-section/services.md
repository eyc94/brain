# :heavy_check_mark: Services: Great and Small

## :round_pushpin: Introduction
Service-oriented architecture and micro-service architecture are popular. The reasons are because:
- Services seem to be strongly decoupled from one another. This is only partially true.
- Services appear to support independence of development and deployment. This is partially true.

## :round_pushpin: Service Architecture?
There's a notion that using services is an architecture. This is untrue. The architecture is defined by how well the boundaries between high-level policy and low-level detail are placed. Services that just separate app behaviors are just expensive function calls.

We are not saying that services *should* be architecturally significant. Services do not define an architecture.

Services are just function calls across process and/or platform boundaries. Some of those are architecturally significant and some aren't.

## :round_pushpin: Service Benefits?
We are going to challenge the current popular orthodoxy of service architecture.

### The Decoupling Fallacy
One supposed benefit is that breaking a system into services decouples all services from each other. This is because each service runs in a different process or processor. So, those services do not have access to each other's variables.

This is partially true. However, they can still share resources within a processor or network. They are strongly coupled to the data they share.

Imagine that a new field is added to the data record passed between services. Every service that uses that field must change. Those services are strongly coupled to the data record, and indirectly coupled to each other.

Service interfaces are the same as function interfaces.

### The Fallacy of Independent Development and Deployment
Another supposed benefit is that services can be owned and dedicated to a team. This is presumed to be *scalable*. It is believed that large enterprise systems can be created from dozens, hundreds, or even thousands of independently developable and deployable services.

There is some truth. First, history has shown that large enterprise systems can scale well from monoliths and component-based systems and service-based systems. So, services are *not* the only way to build scalable systems.

The decoupling fallacy means that services cannot always be independently developed, deployed, and operated.

## :round_pushpin: The Kitty Problem

## :round_pushpin: Objects To The Rescue

## :round_pushpin: Component-Based Services

## :round_pushpin: Cross-Cutting Concerns
