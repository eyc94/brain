# :heavy_check_mark: Java Stack
*Last Updated: 1/24/2023*

![Image of Stack class diagram](../../../images/data-structures/linear/stack/stack-class-diagram.png)

## :round_pushpin: Summary
- Java collection framework provides a `Stack` class that implements the stack data structure.
- The class extends the `Vector` class.
  - Can also be referred to as a sub-class of `Vector`.
- Supports one default constructor.

## :round_pushpin: Java Stack vs Java Deque
- The `Deque` is a double ended queue.
  - Supports inserting and removing elements at both ends.
  - More complete and consistent set of stack operations.

## :round_pushpin: Operations (API)
- [Documentation](https://docs.oracle.com/javase/7/docs/api/java/util/Stack.html)
- Common operations:
  - `push`
  - `pop`
  - `peek`
  - `size`
  - `isEmpty`

## :round_pushpin: Examples
- Instantiate:
```java
Stack<Integer> stack = new Stack<>();
```

- Common operations:
```java
Stack<Integer> stack = new Stack<>();
stack.push(1); // [1]
stack.push(2); // [1, 2]
stack.push(3); // [1, 2, 3]
System.out.println(stack.peek()) // 3
stack.pop(); // [1, 2]
stack.pop(); // [1]
System.out.println(stack.peek()) // 1
```
