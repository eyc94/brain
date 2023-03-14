# :heavy_check_mark: The Main Component

## :round_pushpin: Introduction
In every system, there is one component that creates, coordinates, and oversees the others. This is the `Main` component.

## :round_pushpin: The Ultimate Detail
The `Main` component is the ultimate detail. It is the lowest-level policy.

It is the initial entry point of the system. Nothing, other than the OS, depends on it.

It creates all Factories, Strategies, and other global facilities, and hand them over to the high-level abstract portions of the system.

It's the dirtiest of all components. It is the dirty low-level module in the outermost circle of the clean architecture. It loads everything up for the high level system, and then hands control over to it.
