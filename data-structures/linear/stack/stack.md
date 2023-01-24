# :heavy_check_mark: Stack
*Last Updated: 1/24/2023*

![Image of a stack](../../../images/data-structures/linear/stack/stack.png)

## :round_pushpin: Summary
- Linear data structure.
- LIFO (last in first out).
- Operations only possible in one end.
- Common operations are push and pop.

## :round_pushpin: Characteristics
- Implemented by an array or linked list.
- Elements inserted first will be popped last.
- If the space in a stack is full, any attempts to add more elements results in stack overflow.

## :round_pushpin: Implementations
- Can be implemented by an array or linked list.
- A dynamically resizable array has amortized constant time operations.
- A linked list also has constant time operations.

## :round_pushpin: Operations
- Stacks support `push` and `pop` operations.
  - Items are pushed on a stack and popped from a stack.
  - Popping from an empty stack results in `null` returns or exceptions.
- There is also the `peek` method where it returns the top of the stack without popping.
- Assume that the stack has size `n`.
### Push
- Constant time operation: `O(1)`.

### Pop
- Constant time operation: `O(1)`.

### Peek
- Constant time operation: `O(1)`.

## :round_pushpin: Java Syntax/Libraries
- Java has a `Stack` class: [Documentation](https://docs.oracle.com/javase/7/docs/api/java/util/Stack.html)
  - [Notes](java-stack.md)
- Java has a `Deque` interface: [Documentation](https://docs.oracle.com/javase/7/docs/api/java/util/Deque.html)
  - [Notes](java-deque.md)
- Java has an `ArrayDeque` implementation of the `Deque` interface: [Documentation](https://docs.oracle.com/javase/7/docs/api/java/util/ArrayDeque.html)
  - [Notes](java-arraydeque.md)
